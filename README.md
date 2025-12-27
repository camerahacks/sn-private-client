# Supernote Private Cloud Python Client

A Python client for connecting to a Supernote Private Cloud Instance. Useful for automating tasks like uploading content to your Supernote device.

Requires Python 3.10+

## Usage and Examples

Setup the client anc connect to private cloud.
```python
import snpvclient
snclient = snpvclient.SNPClient('https://supernote.example.com')
snclient.login('email@example.com', 'password')
```

Get root folder and file list
```python
root_folder = snclient.getList()
```

Get list of folders and files for a specific ```id```
```python
folder_list = snclient.getList('78236046000054508') # id
```

Upload a file
```python
upload = snclient.upload(file_path, directoryId)
```