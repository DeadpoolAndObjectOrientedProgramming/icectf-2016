# IceCTF 2016 : Move Along

**Category:** Web
**Points:** 30
**Solves:** 1183
**Description:**

[This site](http://move-along.vuln.icec.tf/) seems awfully suspicious, do you think you can figure out what they're hiding?

## Write-up

We noticed the image on the site is hosted from a subfolder `/move_along/`. Checking out the subfolder directly yielded this directory list and the folder `0f76da769d67e021518f05b552406ff6/` there includes a `secret.jpg` image with the solution.

![cat](https://camo.githubusercontent.com/388308d38acfd822f65cd93ffe0644028db20efa/687474703a2f2f6d6f76652d616c6f6e672e76756c6e2e696365632e74662f6d6f76655f616c6f6e672f30663736646137363964363765303231353138663035623535323430366666362f7365637265742e6a7067)

See [#6](https://github.com/ikornaselur/project-firewater/issues/6)
