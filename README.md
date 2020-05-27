# sallyapi

doc.yaml: for web admin panel

doc_v2.yaml: for mobile client

Recommend using swagger-viewer to visualise the yaml document with Chrome
https://chrome.google.com/webstore/detail/swagger-viewer/nfmkaonpdmaglhjjlggfhlndofdldfag

# Reminder
1. For updating avatar icon, call the /file/uploadToken api and upload the image to S3, then call /user/profile api to upload the file KEY. To get the user's profile by calling GET /user/profile, the avatar_url field will be changed to the url that access the image.

2. The correct way to create user account: 
  i. create the user
  ii. create the shop, with pic_guid = the guid of the newly created user
  iii. update user's information : PATCH /api/user/profile
 
3. Before a mobile user can call the SOP step api (get current step/ proceed step in doc.yaml), the admin must have already assigned the doctor's duty of the current month.
