This document details the procedure to include the spanish books on the
smile plug.

Clone this repo and from the console inside the folder follow the
following steps.

Copy the logo in the assets folder

```bash
scp gutenberg.png root@10.1.0.1:/usr/share/nginx/html/assets/
```
To test if the image was loaded go to
`http://10.1.0.1/assets/img/gutenberg.png` on your browser.

Upload the js file to the smile with secure copy:

Right now going to `http://10.1.0.1` should display the following

![picture of default smile installation](/imgs/pic1.png)

To display the next element run on the console the following code.

```bash
scp smile_access.min.js root@10.1.0.1:/usr/share/nginx/html/js/
```
After this step, the index page `http://10.1.0.1` should appear as:

![picture of smile installation including project gutenberg](/imgs/pic2.png)

proceed to do ssh to box following the procedure.
```bash
ssh root@10.1.0.1
```
when requesting a password introduce `root`

```bash
cd /usr/share/nginx/html/
mkdir gutenberg
```

then you can exit and copy the files to the new created folder on the
box.

```bash
scp -r files root@10.1.0.1:/usr/share/nginx/html/gutenberg/
scp index.html root@10.1.0.1:/usr/share/nginx/html/gutenberg/
```

You should be able to click on the project gutenberg button and see all
the books
