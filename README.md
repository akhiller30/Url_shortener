# URL Shortener
I implemented this API using Python as the langauge, and Flask as the
framework. I also made a database using SQLite to keep track of the mappings
from the encoded url to the original url.

## Running the Project
You can run the project from the command line by typing the following command:

```console
akhilarunachalam@Akhils-MacBook-Air-6 URL_Shortener % python3 url.py
```

After typing in the command, the following output will display information such
as where the script is running on the local machine. The following url is where 
the project was running on in my machine. We will be testing the code by 
pasting the url, the specified endpoint, and proper parameters on a web browser 
such as Google Chrome to see if the API works as expected.

```console
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

## `encode` Endpoint
This endpoint expects a parameter, `url`, for the url that is expected to be
encoded. If no `url` parameter is passed in, an error will be thrown.

![alt text](https://github.com/akhiller30/Url_shortener/blob/main/Images/No_parameter.png "No Url Parameter")

If the url parameter is passed in, then the encoded url will be displayed in 
JSON format.

![alt text](https://github.com/akhiller30/Url_shortener/blob/main/Images/Encode.png "Encode success")

## `decode` Endpoint
Similar to the `encode` endpoint, this endpoint requires a parameter to be 
passed in as well.

If the url parameter is passed in, then the decoded url will be displayed in 
JSON format.

![alt text](https://github.com/akhiller30/Url_shortener/blob/main/Images/Decode.png "Decode success")

However, if there is no mapping from the encoded url to the original url in the
database, an error will be thrown. This is because the url that is passed in 
(encoded url) was never generated by the `encode` endpoint, so the database has
no knowledge about the original url.

![alt text](https://github.com/akhiller30/Url_shortener/blob/main/Images/No_mapping.png "No Mapping Exists")
