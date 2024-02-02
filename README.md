# SecurityBoat-2024-CTF-February-Challenge

1.First, I visited the Website http://ctf.securityboat.net/

2.Then i have done brute-fore to get hidden directories i got /admin/ directory in that their are many files to do work on.
![admindir](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/db0791fd-3943-4c14-ac87-a0e510d92741)


3.Then, I intercept the /edituser.html in BurpSuite but i cant use that the functionality to update the user because i dont have access to admin account.


4.After the request in intercepted then i have done some request manupulation by deleting the PHPSESSIONID header and also response manipulaton with false value to true because of this code isLogged=true means authencation in geniune.There is POST request with operation=sessionCheckAdmin after do-intercept response i got false in response but now i have changed that with true.
![js](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/061848c7-bd41-4600-8e4e-9e46e00f614b)

5.Now wo got this response look for point number 8 you will get the idea then do forward and forward
![data200](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/a1f01d56-30cc-4099-ba96-218abd8f4d45)
![true](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/dea93cda-ac0d-4be5-a411-b80c3184653d)



6.got access to edituser.html like this
![edituser](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/b71a9eaf-b993-4f41-9dc3-faa39874bd4f)


7.i put the values input field but i have got error
![error2](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/212f6169-4c26-4002-aad1-9bf6b1a44b25)



8.Then i have done intercept request in burp and send to repeater delete the PHPSESSIONID and added token= parameter before name parameter because in users.html file there is token field to make a user authenticated.
![user](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/322934be-3199-4c54-b7a9-5d51c6f738d8)


9.Click send after this that it we got our flag...
![poc](https://github.com/zaidbhati784/SecurityBoat-2024-CTF-February-Challenge/assets/114328894/7082f705-aefd-4c1c-aca0-cd7ba65856a3)


10.User updated by other account !! Your Flag {!DOR_!S_FUN}
