### 1. download image file
- drawing.flag.svg

### 2. Run `grep` on image id with extended regex flag
```bash
grep -E 'id="[^"]*"' drawing.flag.svg
```
<details>

### returns
```text
   id="svg8"
     id="defs2" />
     id="base"
     showgrid="false"
     id="metadata5">
     id="layer1">
       id="path3713"
       id="path3717"
       id="path3719"
       id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ 2 4 3 7 4 6 7 5 }</tspan></text>
```
</details>

### 3. Concatenate flag text to output
```bash
cat drawing.flag.svg | grep -oP '(?<=>)[^<]+(?=</tspan>)' | tr -d ' \n'
```
