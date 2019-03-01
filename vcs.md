##### Fork
/t (open in a provisional tab, don’t use if you want to open in a normal tab)  
/m (merge operation)  

Diff tool: "$LOCAL" "$REMOTE" "Source" "Target" //t  
Merge tool: "$LOCAL" "$REMOTE" "$BASE" "$MERGED" //m  

$LOCAL El archivo de la rama en la que se está fusionando; no se ve afectado por el proceso de fusión cuando se le muestra.  

$REMOTE El archivo de la rama desde la que se está fusionando; no se ve afectado por el proceso de fusión cuando se le muestra.  

$BASE El ancestro común de $LOCAL y $REMOTE, es decir, el punto en el que las dos ramas empezaron a desviar el archivo considerado; sin ser tocado por el proceso de fusión cuando se le muestra.  

MERGED El archivo parcialmente fusionado, con conflictos; este es el único archivo tocado por el proceso de fusión y, en realidad, nunca se le ha mostrado en meld.  
