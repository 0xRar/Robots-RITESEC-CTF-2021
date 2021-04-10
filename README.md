# Writeup for **Robots** RITESEC CTF 2021
![image](https://user-images.githubusercontent.com/33517160/114279435-5a15e900-9a3d-11eb-828f-a7c07adc4820.png)

- Challenge Name: **`Robots`**
- Category: **`Web`**
- Points: **`100pts`**
## First Look:
This one was really easy but you need to look in the right place and decode every base64 you see,

thats what we get when we enter the website:
![image](https://user-images.githubusercontent.com/33517160/114280631-e676da80-9a42-11eb-8d7b-66e977ae8fa8.png)

but there is one thing, we need to look at the source code:
![image](https://user-images.githubusercontent.com/33517160/114280678-1a520000-9a43-11eb-9a86-d314fa7a894f.png)

nothing much here but we see a plain text `flag.txt` its a file but is it the flag?
we get this base64 encoded text : `VW05aWIzUnpJR0Z5WlNCMFlXdHBibWNnYjNabGNpQXVMaTQ9 = Robots are taking over ...`


## Solution:
but thats nothing its just a rabbit hole, but also the name of the challenge is a big hint, lets check `robots.txt`, there is alot of things here lets filter our search and use `CTRL + F` to search for the word: `flag`:
![image](https://user-images.githubusercontent.com/33517160/114280869-fe9b2980-9a43-11eb-93d3-b440d2bde3df.png)

we got something thats good but when we try to access `Allow: /flag/UlN7UjBib3RzX2FyM19iNGR9` we get 404
and it looks like `UlN7UjBib3RzX2FyM19iNGR9` is a base64 lets decode it, and yes, we got our flag.

Flag: `RS{R0bots_ar3_b4d}`
