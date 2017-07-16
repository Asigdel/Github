# Github
##################### missing valeus in unix rrpalcing with -99 ###################
 awk 'BEGIN { FS = OFS = "\t" } { for(i=1; i<=NF; i++) if($i ~ /^ *$/) $i = -99 }; 1' clean1_DRMS_UFL_Penagaricano_F4_Active.txt_SCS.txt

# how to delete the entire row based on the value of a column in unix file
```
awk '$8 == "" { next } { print }' "Final2_Phenotype_milk_Testday7_Lac1.2.3.txt" | more
```
#### how to change the value of a column based on the conditions
awk '{ if ($6 >= 1 && $6 <= 20){ $11=1 };if($6 >= 21 && $6 <= 40){ $11=2 };if($6 >= 41 && $6 <= 60){ $11=3 };if($6 >= 61 && $6 <= 80){ $11=4 };if($6 >= 81 && $6 <= 100){ $11=5 };if($6 >= 101 && $6 <= 120){ $11=6 };if($6 >= 121 && $6 <= 140){ $11=7 } if($6 >= 141 && $6 <= 160){ $11=8 } if($6 >= 161 && $6 <= 180){ $11=9 } if($6 >= 181 && $6 <= 200){ $11=10 } if($6 >= 201 && $6 <= 220){ $11=11 } if($6 >= 221 && $6 <= 240){ $11=12} if($6 >= 241 && $6 <= 260){ $11=13 } if($6 >= 261 && $6 <= 280){ $11=14 } if($6 >= 281 && $6 <= 300){ $11=15 } if($6 >= 301 && $6 <= 320){ $11=16 } if($6 >= 321 && $6 <= 340){ $11=17 }if($6 >= 341 && $6 <= 360){ $11=18 }if($6 >= 361 && $6 <= 380){ $11=19 } print }' Final_Phenotype_milk_Testday7_Lac1.2.3.txt > milkpheno
