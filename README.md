# Algorithm-check_point
FUNCTION cards_sort(cards: ARRAY_OF INTEGER[len];)
VAR
    temp: INTEGER
    swapped: BOOLEAN:= true
BEGIN
    Read(cards)
    WHILE (swapped) DO
        swapped = false

        FOR i FROM 0 TO len-1 STEP 1  DO
            IF (cards[i]> cards[i+1]) THEN
                temp= cards[i]
                cards[i]= cards [i+1]
                cards [i+1] = temp
                swapped=true
            END_IF
        END_FOR
    END_WHILE


    this algorithm is an array with an integer and boolean as its variable. Its a card sorting which has been initializes to false. it states that fro 0 to the length of cards,do. if the cards array is greater than then cards lenght will increment by 1 each time the card loop through. the output will be stored in a variable. in this case, each time the card increment, it will be assigned to true
