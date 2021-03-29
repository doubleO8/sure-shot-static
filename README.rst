Example Run
===========

::

  python -m virtualenv -p python3 venv
  . venv/bin/activate
  pip install sure-shot-static

  mkdir -p public/
  # copy files and folders to public/ ...

  # set AWS credentials if needed ... 
  export AWS_ACCESS_KEY_ID=XXXXXXXXXXX
  export AWS_SECRET_ACCESS_KEY=YYYYYYYYYYYYYY
  export AWS_DEFAULT_REGION=eu-central-1
  export STATIC_ASSETS_BUCKET=xxxx

  sure-shot-static

  2021-03-18 18:06:31 INFO     ----------------------------------------------------------------------------------------------------
  2021-03-18 18:06:31 INFO     Trying to push contents of '/tmp/public' to arn:aws:s3:::xxxx (https://xxxx.s3.eu-central-1.amazonaws.com)
  2021-03-18 18:06:31 INFO     ----------------------------------------------------------------------------------------------------
  2021-03-18 18:06:31 INFO     
  2021-03-18 18:06:31 INFO      + dry/echarts.min.js.br                                        text/javascript (br)
  2021-03-18 18:06:32 INFO        No update needed ...
  2021-03-18 18:06:32 INFO     
  2021-03-18 18:06:32 INFO      + css/bootstrap-4.4.1-and-font-awesome-4.7.0.css.br            text/css (br)
  2021-03-18 18:06:32 INFO        No update needed ...
  2021-03-18 18:06:32 INFO     
  2021-03-18 18:06:32 INFO      + fonts/FontAwesome.otf                                        application/vnd.ms-opentype
  2021-03-18 18:06:33 INFO        No update needed ...
  2021-03-18 18:06:33 INFO     
  2021-03-18 18:06:33 INFO      + fonts/fontawesome-webfont.eot                                application/vnd.ms-fontobject
  2021-03-18 18:06:33 INFO        No update needed ...
  2021-03-18 18:06:33 INFO     
  2021-03-18 18:06:33 INFO      + fonts/fontawesome-webfont.svg                                image/svg+xml
  2021-03-18 18:06:33 INFO        No update needed ...
  2021-03-18 18:06:33 INFO     
  2021-03-18 18:06:33 INFO      + fonts/fontawesome-webfont.ttf                                font/ttf
  2021-03-18 18:06:33 INFO        No update needed ...
  2021-03-18 18:06:33 INFO     
  2021-03-18 18:06:33 INFO      + fonts/fontawesome-webfont.woff                               font/woff
  2021-03-18 18:06:33 INFO        No update needed ...
  2021-03-18 18:06:33 INFO     
  2021-03-18 18:06:33 INFO      + fonts/fontawesome-webfont.woff2                              font/woff
  2021-03-18 18:06:33 INFO        No update needed ...
  2021-03-18 18:06:33 INFO     


Publishing to pypi
==================

::

  poetry publish -r pypi --build
