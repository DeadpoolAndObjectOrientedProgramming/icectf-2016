# IceCTF 2016 : Hidden in Plain Sight

**Category:** ReserveEngineering
**Points:** 45
**Solves:** 842
**Description:**

Make sure you take a real close look at it, it should be right there! `/home/plain_sight/` or download it [here](https://play.icec.tf/problem-static/828644c3ad8ccfa14b86a69dccd36f2b-plain_sight_df5d2c1da50110458fa00d0db6586b23cd67317c7f7b95f4a092d645a4570296)

## Write-up

We started by running the executable through Hex-Rays IDA decompiler. Looking through the disassembled output we noticed a sequence of hex characters out out place

![IMAGE](https://cloud.githubusercontent.com/assets/3537289/17633375/80260b58-60bc-11e6-8d13-bb224142a4d5.jpg)

Converting the hex characters to ascii gave us the flag

![ANOTHER IMAGE](https://cloud.githubusercontent.com/assets/3537289/17633398/a37cacd8-60bc-11e6-840d-bc2ffb0a7394.png)

See [#13](https://github.com/ikornaselur/project-firewater/issues/)
