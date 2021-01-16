import requests
import json
import time

print("Please provide the image link! (It should end with .png or .jpg)")

imgurl = input()


url = "https://microsoft-face1.p.rapidapi.com/detect"

querystring = {"returnFaceAttributes":"age"}

payload = "{\r\"url\": \"" + imgurl + "\"\r}"
headers = {
    'content-type': "application/json",
    'x-rapidapi-key': "88040e26b7mshfb93f474f57abfap1e9699jsnbc54aae19dc5",
    'x-rapidapi-host': "microsoft-face1.p.rapidapi.com"
    }

response = requests.request("POST", url, data=payload, headers=headers, params=querystring)

json_response = response.json()
repository = json_response[0]["faceAttributes"]["age"]

realage = "They are " + str(repository) + " years old!"


print(realage)
time.sleep(5)
