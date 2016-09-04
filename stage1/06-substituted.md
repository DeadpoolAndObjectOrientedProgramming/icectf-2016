# IceCTF 2016 : Substituted

**Category:** Cryptography
**Points:** 30
**Solves:** 1217
**Description:**

We got a substitute flag, I hear they are pretty lax on the rules... [crypted.txt](https://play.icec.tf/problem-static/crypted_a888cc3cc9e064482ab8b61d0b19ca0b1b1ce88238c63f03c306d33947cf113b.txt)

crypted.txt contents:
```
Lw!

Gyzvecy ke WvyVKT!

W'zz by reso dsbdkwksky tzjq teo kly ujr. Teo keujr, gy joy dksurwmq bjdwv vorakeqojalr jmu wkd jaazwvjkwemd. Vorakeqojalr ljd j zemq lwdkeor, jzklesql gwkl kly juxymk et vecaskyod wk ljd qekkym oyjzzr vecazwvjkyu. Decy dwcazy ezu vwalyod joy kly Vjydjo vwalyo, kly Xwqymyoy vwalyo, kly dsbdkwkskwem vwalyo, glwvl wd klwd emy, jmu de em. Jzcedk jzz et klydy vwalyod joy yjdwzr boeiym keujr gwkl kly lyza et vecaskyod. Decy myg ymvorakwem cykleud joy JYD, kly vsooymk dkjmujou teo ymvorakwem, jzemq gwkl ODJ. Vorakeqojalr wd j xjdk twyzu jmu wd xyor wmkyoydkwmq klesql. De iwvi bjvi, oyju sa em decy veez vwalyod jmu ljxy tsm!

El jmu teo reso oyveoud cr mjcy wd WvyVKT{jzgjrd_zwdkym_ke_reso_dsbdkwksky_tzjqd}.
```

## Write-up

Simple substitution cipher. We just found a simple [solver online](http://quipqiup.com/index.php), which gave us the solution within a second:

```
Hi!

Welcome to IceCTF

I'll be your substitute flag for the day. For today, we are studying basic cryptography and its applications. Cryptography has a long history, although with the advent of computers it has gotten really complicated. Some simple old ciphers are the Caesar cipher, the Vigenere cipher, the substitution cipher, which is this one, and so on. Almost all of these ciphers are easily broken today with the help of computers. Some new encryption methods are AES, the current standard for encryption, along with RSA. Cryptography is a vast field and is very interesting though. So kick back, read up on some cool ciphers and have fun!

Oh and for your records my name is IceCTF{always_listen_to_your_substitute_flags}.
```

See [#8](https://github.com/ikornaselur/project-firewater/issues/8)
