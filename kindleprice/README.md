# Files

* lab.network -- Podman network containing communication between containers.
* ntfy.container -- container to send notification, on errors on in case of
price drops
* kindleprice.container -- Main container for checking prices of books.
It will add new books dropped to -- `/srv/new_books.txt` file inside volume
