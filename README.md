# Writeup for **Robots** RITESEC CTF 2021
![image](https://user-images.githubusercontent.com/33517160/114281089-03aca880-9a45-11eb-83b9-3e77626f37f7.png)


- Challenge Name: **`Robots`**
- Category: **`Web`**
- Points: **`100pts`**
## First Look:
This one was really easy but you need to look in the right place and decode every base64 you see,

thats what we get when we enter the website:

![image](https://user-images.githubusercontent.com/33517160/114281113-32c31a00-9a45-11eb-9998-fc5f709e67ce.png)


but there is one thing, we need to look at the source code:
![image](https://user-images.githubusercontent.com/33517160/114281128-50907f00-9a45-11eb-8a27-65525b5bf810.png)


nothing much here but we see a plain text `flag.txt` its a file but is it the flag?
we get this base64 encoded text : `VW05aWIzUnpJR0Z5WlNCMFlXdHBibWNnYjNabGNpQXVMaTQ9 = Robots are taking over ...`


## Solution:
but thats nothing its just a rabbit hole, but also the name of the challenge is a big hint, lets check `robots.txt`, there is alot of things here lets filter our search and use `CTRL + F` to search for the word: `flag`:

![image](https://user-images.githubusercontent.com/33517160/114281147-6a31c680-9a45-11eb-8eaa-cdce22369210.png)

we got something thats good but when we try to access `/flag/UlN7UjBib3RzX2FyM19iNGR9` we get 404
and it looks like `UlN7UjBib3RzX2FyM19iNGR9` is a base64 lets decode it, and yes, we got our flag.

Flag: **`RS{R0bots_ar3_b4d}`**
