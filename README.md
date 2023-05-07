# Albumy

*Capture and share every wonderful moment.*

> Example application for *[Python Web Development with Flask](https://helloflask.com/en/book/1)* (《[Flask Web 开发实战](https://helloflask.com/book/1)》).

Demo: http://albumy.helloflask.com

![Screenshot](https://helloflask.com/screenshots/albumy.png)
## Create Azure Account to use Computer Vision API
1) Sign up for a free account @ https://azure.microsoft.com/en-us/free/ 
2) From Homepage , go to Computer Vision
3) Select Create
4) Create an Instance with the basic given configurations
5) This instance will now show under your computer vision tab
6) Open the instance and copy the endpoint given . You will need this later to add in your config.json
7) Select Manage keys
8) Copy the first key. You will need to put this key in your config.json (below steps).


## Installation

clone:
```
$ git clone https://github.com/greyli/albumy.git
$ cd albumy
```
create & activate virtual env then install dependency:

with venv/virtualenv + pip:
```
$ python -m venv env  # use `virtualenv env` for Python2, use `python3 ...` for Python3 on Linux & macOS
$ source env/bin/activate  # use `env\Scripts\activate` on Windows
$ pip install -r requirements.txt
```
or with Pipenv:
```
$ pipenv install --dev
$ pipenv shell
```
Use your Azure API and API key as such:
1) create a file 'config.json' within albumy.
Its path will look like this -> .../i1-albumy-techna08/albumy/config.json

Use the below format and fill in the API endpoint and key

{
    "subscription_key":"yourKey",
    "endpoint":"yourEndpoint"
}

```
generate fake data then run:
```
$ flask forge
$ flask run
* Running on http://127.0.0.1:5000/

If flask forge gives an error , try : python3 -m flask forge 
AND
python3 -m flask run
```
Test account:
* email: `admin@helloflask.com`
* password: `helloflask`

## License

This project is licensed under the MIT License (see the
[LICENSE](LICENSE) file for details).

## How to test ML Features
1) Alternative Text
Upload image -> save image -> go to feed -> select your uploaded image -> you will see alt text in the description.
Additonally, you can go to Developer tools and Inspect the HTML.
When you hover over the image , you will see the Alt Text

2) Image Search
Upload image -> save image -> go to feed -> select your uploaded image -> you will see the auto generated tags
When you search for the image in the search bar, you will find your images in the tagged section.