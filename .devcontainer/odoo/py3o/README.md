# OCA/reporting-engine

https://github.com/OCA/reporting-engine

- report_py3o:  
Reporting engine based on Libreoffice (ODT -> ODT, ODT -> PDF, ODT -> DOC, ODT -> DOCX, ODS -> ODS, etc.)
- report_py3o_fusion_server:  
Let the fusion server handle format conversion.

# py3o Source Distributions

- py3o.formats==0.3
- py3o.fusion==0.8.9
- py3o.renderclient==0.3
- py3o.renderers.juno==0.8.1
- py3o.renderserver==0.5.2
- py3o.template==0.10.0
- py3o.types==0.1.1

# Missing README.md file in py3o.renderers.juno

The installation of `py3o.renderserver` fails because the dependent `py3o.renderers.juno` package is missing the **`README.md`** file.

Therefore, install `py3o.renderers.juno` manually as follows:

```bash
mkdir py3o.renderers.juno
cd py3o.renderers.juno
curl -o py3o.renderers.juno-0.8.1.tar.gz \
    https://files.pythonhosted.org/packages/17/32/5954c32dc1d0e568410c3dcb4f203f0c9d10dabf73b3e78acb90ee639e84/py3o.renderers.juno-0.8.1.tar.gz
tar -zxvf py3o.renderers.juno-0.8.1.tar.gz -C ./ --strip-components 1
touch README.md
python setup.py build
sudo python setup.py install
cd ..
sudo rm -rf py3o.renderers.juno
```

# Project Home Moved
The project hosting has moved to https://orus.io/florent.aide

**dockers**
https://orus.io/xcg/docker
