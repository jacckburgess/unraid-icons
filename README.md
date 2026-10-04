# unraid-icons

Icons for my Unraid Docker containers.

Unraid downloads container icons on the server using the template's **Icon URL**, without any authentication, so the icons need to be publicly reachable. The app source code stays in private repos; this repo holds only the images.

## Icons

| Container  | File                    |
|------------|-------------------------|
| jbooks     | `icons/jbooks.png`      |
| jcook      | `icons/jcook.png`       |
| jnutrition | `icons/jnutrition.png`  |
| jbudget    | `icons/jbudget.png`     |

## Usage

In Unraid, go to **Docker → (container) → Edit → Icon URL** and set:

```
https://raw.githubusercontent.com/jacckburgess/unraid-icons/main/icons/<name>.png
```

For example:

```
https://raw.githubusercontent.com/jacckburgess/unraid-icons/main/icons/jbooks.png
```

Click **Apply**.

## Adding an icon

1. Add a square PNG (256×256 or larger) to `icons/`, named after the container.
2. Commit and push to `main`.
3. Set the container's Icon URL as above.

Unraid caches icons, so after replacing an existing image you may need to clear the cached copy (`/var/lib/docker/unraid/images/`) or re-apply the container for the change to show.
