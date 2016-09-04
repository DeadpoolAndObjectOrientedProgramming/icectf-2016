# IceCTF 2016 : Rotated!

**Category:** Cryptography
**Points:** 20
**Solves:** 1453
**Description:**

They went and ROTated the flag by 5 and then ROTated it by 8! The scoundrels! Anyway once they were done this was all that was left VprPGS{jnvg_bar_cyhf_1_vf_3?} 

## Write-up

It's just a rotation cipher, where we "rotate" each letter by `5+8=13` in the alphabet. 13 is the usual number of rotations done in this simple cipher, that's why the cipher is actually called ROT13. There's a simple website to try it out at [www.rot13.com](http://www.rot13.com/).

See [#4](https://github.com/ikornaselur/project-firewater/issues/4)
