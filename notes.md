### RPS
```sh
#!/bin/bash

while [ true ]; do
        c_turn=""
        p_turn=""
        los=$(( $RANDOM % 3+1 ))

        if [ $los == 1 ]; then
                c_turn="r"
        elif [ $los == 2 ]; then
                c_turn="p"
        else [ $los == 3 ];
                c_turn="s"
        fi

        read -p "What move on your part? Choose 'r' 'p' or 's'" p_turn

        if [ $p_turn == $c_turn ]; then
                echo "it's a tie!"
        elif [ $p_turn == "r" ] && [ $c_turn == "p" ]; then
                echo "you lost"
        elif [ $p_turn == "r" ] && [ $c_turn == "s" ]; then
                echo "good job!"
        elif [ $p_turn == "p" ] && [ $c_turn == "s" ]; then
                echo "you lost!"
        elif [ $p_turn == "p" ] && [ $c_turn == "r" ]; then
                echo "good job!"
        elif [ $p_turn == "s" ] && [ $c_turn == "r" ]; then
                echo "you lost!"
        elif [ $p_turn == "s" ] && [ $c_turn == "p" ]; then
                echo "good job!"
        fi

        read -p "Do you want to exit? Enter 'y', otherwise press 'n'" end
        if [ $end == "y" ]; then
                break
        fi
done
```

### CONVERTER
```sh

#!/bin/bash

VALUE=$1
INPUT_UNIT=$2
OUTPUT_UNIT=$3
KG_2_LBS=2.20462
LBS_2_KG=0.453592
KM_2_MILES=0.621371
MILES_2_KM=1.60934

if [ -z ${VALUE} ]; then
        echo "USE:: converter.sh VALUE INPUT_UNIT OUTPUT_UNIT"
        read -p "What is the value you want to convert? " VALUE
        echo ${VALUE}
fi
if [ -z ${INPUT_UNIT} ]; then
        read -p "What is the unit you want to convert from? " INPUT_UNIT
        echo ${INPUT_UNIT}
fi
if [ -z ${OUTPUT_UNIT} ]; then
        read -p "What is the unit you want to convert to? " OUTPUT_UNIT
        echo ${OUTPUT_UNIT}
fi

echo "Entered values to count: VALUE=${VALUE}, INPUT_UNIT=${INPUT_UNIT}, OUTPUT_UNIT=${OUTPUT_UNIT}"

if [ ${INPUT_UNIT} == "kg" ]; then
        if [ ${OUTPUT_UNIT} == "lbs" ]; then
                lbs=$(echo "${VALUE} * ${KG_2_LBS}" | bc)
                echo Value ${VALUE} kg is equal to ${lbs} lbs.
        fi
fi

if [ ${INPUT_UNIT} == "lbs" ]; then
        if [ ${OUTPUT_UNIT} == "kg" ]; then
                kg=$(echo "${VALUE} * ${LBS_2_KG}" | bc)
                echo Value ${VALUE} lbs is equal to ${kg} kg.
        fi
fi

if [ ${INPUT_UNIT} == "km" ]; then
        if [ ${OUTPUT_UNIT} == "miles" ]; then
                MILES=$(echo "${VALUE} * ${KM_2_MILES}" | bc)
                echo Value ${VALUE} km is equal to ${MILES} miles.
        fi
fi

if [ ${INPUT_UNIT} == "miles" ]; then
        if [ ${OUTPUT_UNIT} == "km" ]; then
                KM=$(echo "${VALUE} * ${MILES_2_KM}" | bc)
                echo Value ${VALUE} miles is equal to ${KM} km.
        fi
fi

# temperatura

if [ ${INPUT_UNIT} == "C" ]; then
        if [ ${OUTPUT_UNIT} == "F" ]; then
                F=$(echo "(${VALUE} * 9/5) + 32" | bc)
                echo Value ${VALUE}C is equal to ${F}F.
        fi
fi


if [ ${INPUT_UNIT} == "F" ]; then
        if [ ${OUTPUT_UNIT} == "C" ]; then
                C=$(echo "(${VALUE} - 32) * 5/9" | bc)
                echo Value ${VALUE}F is equal to ${C}C.
        fi
fi
```

### GENERATOR
```sh
#!/bin/bash

NAME=$1
AUTHOR=$2
DATE=$3

if [ -z ${NAME} ]; then
        echo "use: generator.sh NAME AUTHOR DATE"
        read -p "What is the name of the project? " NAME
        echo ${NAME}
fi
if [ -z ${AUTHOR} ]; then
        read -p "What is the author of said project? " AUTHOR
        echo ${AUTHOR}
fi
if [ -z ${DATE} ]; then
        read -p "What is the starting date of the project? " DATE
        echo ${DATE}
fi


read -p "Please, enter the description of the project " DESCRIPTION


echo "# Project $NAME " > README.md
echo "" >> README.md
echo "### Author of the project: ${AUTHOR}" >> README.md
echo "" >> README.md
echo "### The starting date of the project: ${DATE}" >> README.md
echo "" >> README.md
echo "### Description: " >> README.md
echo "${DESCRIPTION}" >> README.md
```
