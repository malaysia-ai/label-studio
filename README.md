## Label Studio for Malaysia AI

- This repo is for Malaysia AI use to collect annotation

## how-to deploy

1. Install local development,

```bash
# install miniconda
pip install -e .
python label_studio/manage.py migrate
python label_studio/manage.py runserver
```

2. Install PM2,

```bash
sudo apt install npm -y
sudo npm install pm2 -g
```

3. Run as daemon using PM2,

```bash
pm2 start "/home/ubuntu/miniconda3/envs/label/bin/python3.8 /home/ubuntu/label-studio/label_studio/manage.py runserver"
pm2 startup
sudo env PATH=$PATH:/usr/bin /usr/local/lib/node_modules/pm2/bin/pm2 startup systemd -u ubuntu --hp /home/ubuntu
pm2 save
```

## Citation

```tex
@misc{Label Studio,
  title={{Label Studio}: Data labeling software},
  url={https://github.com/heartexlabs/label-studio},
  note={Open source software available from https://github.com/heartexlabs/label-studio},
  author={
    Maxim Tkachenko and
    Mikhail Malyuk and
    Nikita Shevchenko and
    Andrey Holmanyuk and
    Nikolai Liubimov},
  year={2020-2021},
}
```

## License

This software is licensed under the [Apache 2.0 LICENSE](/LICENSE) © [Heartex](https://www.heartex.ai/). 2020-2021

<img src="https://github.com/heartexlabs/label-studio/blob/master/images/opossum_looking.png?raw=true" title="Hey everyone!" height="140" width="140" />
