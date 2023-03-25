# TIKTOK Signature FREE API

## How To Use

### API Request

```py
import requests

url = 'https://tiktok-signature.onrender.com/api/signature/' # API url

data = {
    'url': '', # TikTok url want to sign
    'userAgent': '', # Paste your browser userAgent
    'version': '2', # choice 1 or 2
    'Token': 'main-HH7H@Signature', # API Token
    'data': '', # TikTok request body
    'Bogus': True, # make True to generate
    'msToken': True, # ...
    '_signature': True # ...
}

response = requests.post(url=url,data=data).json()

print(response)
```

### Response

```json
{
    "status": "ok",
    "code": 200,
    "new_url": "https://www.tiktok.com/api/uniqueid/check/?aid=1988&app_language=en&app_name=tiktok_web&browser_language=en-US&msToken=DYgkLel=ggW6zDcsocKf7Ks3MkkrGwGd6d=VqpXAfee1HGmK4dKLX92cHe8Y4RRBrRSkKeNiaWst1bp3WSGLUmyV7b0ZBGtyRe2ymeUtznbsDXloiUonMKFgszcCX=PMGsKcShOgLwOZzH=Y&X-Bogus=DFSzswSOBVkANnVUtcFBhyZSts-M&_signature=_02B4Z6wo00001GeWSmwAAIDCFhY6xSHxJgRnpkbAAH4Ccd",
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.2 Safari/605.1.15", "version": "2",
    "msToken": "DYgkLel=ggW6zDcsocKf7Ks3MkkrGwGd6d=VqpXAfee1HGmK4dKLX92cHe8Y4RRBrRSkKeNiaWst1bp3WSGLUmyV7b0ZBGtyRe2ymeUtznbsDXloiUonMKFgszcCX=PMGsKcShOgLwOZzH=Y",
    "X-Bogus": "DFSzswSOBVkANnVUtcFBhyZSts-M",
    "_signature": "_02B4Z6wo00001GeWSmwAAIDCFhY6xSHxJgRnpkbAAH4Ccd"
}
```

## detail

Two X-Bogus Version Available:
    Version 1: `DFSzKwjOFnxANxPQtcF6P9w4/MVQ` style changes by time
    Version 2: `DFSzswSOFxUANnVUtcF6OyZStsRP`

POST Method:
    no't all TikTok api supported this X-Bogus versions
    many TikTok api return vaild response and sometimes no't

## NOTE

API Support Douyin(TikTok of China)
