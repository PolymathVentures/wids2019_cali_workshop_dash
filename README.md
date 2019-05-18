# Install 


## Basic setup

```
git clone https://github.com/PolymathVentures/wids2019_cali.git
cd wids2019_cali
python3 -m venv venv
source venv/bin/activate

pip3 install -r requirements.txt
```

## Run dashboard

```
python3 app.py
```

## Deployment

### Add Authentification

```
pip install dash_auth
```

````
import dash_auth

VALID_USERNAME_PASSWORD_PAIRS = [
    ['hello', 'world']
]

app = dash.Dash(__name__, external_stylesheets=external_stylesheets)
auth = dash_auth.BasicAuth(
    app,
    VALID_USERNAME_PASSWORD_PAIRS
)
```

### Deploy on heroku

```
curl https://cli-assets.heroku.com/install.sh | sh
pip freeze > requirements.txt
heroku create wids2019_cali
git push heroku master
```




