# Github
##################### missing valeus in unix rrpalcing with -99 ###################
 awk 'BEGIN { FS = OFS = "\t" } { for(i=1; i<=NF; i++) if($i ~ /^ *$/) $i = -99 }; 1' clean1_DRMS_UFL_Penagaricano_F4_Active.txt_SCS.txt
