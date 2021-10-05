# cloud-post-client-qt
qt project sending http post api to aws api end point. The reason i call this project cloudpost is that this is part of another projects. 

## Download and install locally
1. `simply clone the project and using qtcreator to open it`

## Config api request header and body
The following lines can be replaced for typical needs:
```
    const QUrl url(QStringLiteral("https://123.execute-api.ap-east-1.amazonaws.com/default/cloudpost"));
    QNetworkRequest request(url);
    request.setHeader(QNetworkRequest::ContentTypeHeader, "application/json");

    QJsonObject obj;
    obj["s3bucket"] = "cloudpost-receiver";
    obj["s3key"] = "aaa2.cls";
    obj["s3region"] = "ap-east-1";
```

## Run it!
You may customerize qt code to add more widgets. I simpley nested api request code in the main function. 
