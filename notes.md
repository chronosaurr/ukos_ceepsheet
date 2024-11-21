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



