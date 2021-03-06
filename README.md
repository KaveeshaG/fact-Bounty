# Fact Bounty

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/7574ef8d36d8451fa979a42e2884504f)](https://app.codacy.com/app/ivantha/fact-Bounty?utm_source=github.com&utm_medium=referral&utm_content=scorelab/fact-Bounty&utm_campaign=Badge_Grade_Settings)

The recent decade has witnessed the birth of social media ecosystems that brings social organizations, media content and various stakeholders together, and now it appears significant advantages of comprehensiveness, diversity and wisdom that provide users with higher quality of experiences. Meanwhile, social media ecosystems suffer from security, privacy and trustworthiness threats. How to leverage the power of intelligent crowds to improve the ecosystem’s efficacy and efficiency, as well as ensure its security and privacy become burning and challenging issues.

#### Fact Bounty is a crowd sourced fact checking platform.

# User Guide

#### How to Setup

Clone the repository.

`git clone https://github.com/scorelab/fact-Bounty.git`

Change directry to the folder.

`cd fact-Bounty/`

## Set up react server

Run npm install in fact-bounty-client folder.

```
 cd fact-bounty-client/
 npm install
 ```

## Set up flask server

### Technologies required
*   **[Python3](https://www.python.org/downloads/)** - A programming language that lets you work more quickly (The universe loves speed!).
*   **[Flask](flask.pocoo.org/)** - A microframework for Python based on Werkzeug, Jinja 2 and good intentions
*   **[Virtualenv](https://virtualenv.pypa.io/en/stable/)** - A tool to create isolated virtual environments
*   **[SQLite](https://www.sqlite.org/)** - An in-process library that implements a self-contained, serverless, zero-configuration, transactional SQL database engine
*   **[Elasticsearch](https://www.elastic.co/downloads/elasticsearch)** - A search engine based on the Lucene library
*   Minor dependencies can be found in the requirements.txt file.

### Installation / Usage
 * First ensure you have python3 globally installed in your computer. If not, you can get python3 [here](https://www.python.org).

 * After this, ensure you have installed virtualenv globally as well. If not, run this:
    ```
    $ pip install virtualenv
    ```

 * #### Dependencies

    1. Create and fire up your virtual environment in python3:
    ```
        $ virtualenv -p python3 venv
        $ source venv/bin/activate
    ```
        For *Windows* you can use - 
    ```
        $ venv/Scipts/activate.bat
    ```

*   #### Environment Variables
    Create a .env file and add the following:
    ```
	   export FLASK_APP="app.py"
	   export FLASK_ENV="development"
	   export SECRET_KEY="some-very-long-string-of-random-characters-CHANGE-TO-YOUR-LIKING"
	   export FLASK_CONFIG="development"
    ```

    Save the file.

*   #### Install your requirements
    ```
        (venv)$ pip install -r requirements.txt
    ```

*   #### Running It
    On your terminal, run the server using this one simple command:
    ```
        (venv)$ flask run
    ```

*   #### Add sample data
    Browse to db folder and run:
    ```
        (venv)$ python add_es.py
    ```


### How to Use

Use two terminals, one for fact-bounty-flask and the other for fact-bounty-client.

Run the flask server in the fact-bounty-flask folder:
    
`(venv)$ flask run`

start the npm server in fact-bounty-client directory.

`npm start`

And use [localhost:3000](https://) to browse.


> **NOTE**: This version is only supporting for Chrome browser. And make sure to instal the extension -> Redux Dev Tools in chrome extension library.
>

### Running with Docker

1. Change the MongoDB url to user local mongodb database url in *fact-Bounty/fact-bounty-server/config/keys-example.js*.
2. In the root of the project directory, run `docker-compose build`
   - If you are on Linux machine, execute the following steps to install compose. 
     ```
     sudo curl -L https://github.com/docker/compose/releases/download/1.17.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
     sudo chmod +x /usr/local/bin/docker-compose
     ```
3. Once build completes, run `docker-compose up`

# How to Contribute

- First fork the repository and clone it.
- You can open issue regarding any problem according to the given issue template.
- Make changes and do the PR according to the given template.
