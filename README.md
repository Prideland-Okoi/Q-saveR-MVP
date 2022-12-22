# ALX-MVP-Project

MVP Idea: Sales Planet / A sales inventory Management Portal
======================================

A web application that will allow a user to generate QR Code (static and dynamic) for  all varieties of products(url, vCard, file, social media, google form , multi urls, mp3, wifi, etc.) with ease.

### Notes
- Upload form
    - Upload photo
    - upload app 
    - Upload url
    - upload wifi
    - Upload pdf
    - upload social media
- hub
    - Thumbnail grid view.
    - On upload, a new entry is created with a default image to indicate work in progress.
    - When job is finished, thumbnail updates to show new post.
- Detailed single image view
    - Larger representation of image
    - Favs?

### Routes

- `/`: Index, gallery
    - `GET`: Display grid view of qr image generated.
- `/api/hub/<int:qr-imageid>`
    - `GET`: Send qr-image metadata.
     - `POST`: Send qr-image metadata.
      - `PUT`: modify qr-image metadata.
    - `DELETE`: Delete the qr-image with this id.
- `/api/qr-images`
    - `GET`: Return a list of all images.
    - `POST`: Post a new image.
        - This should return 201 when the job is created.
        - . When job is done, retrieve image and update thumbnail/image data.

### Schema

- `qr-image`
    - `metadata`
        - `id`
        - `timestamps`
    - `data`

