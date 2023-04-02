/*  
Coding IF-THEN-ELSE
*/  


DO $GO$
    DECLARE
        -- define your input here.  We'll do better later.
        lvLetter CHAR(1) := 'M';
    BEGIN
        -- You may copy this if you wish.
        IF lvLetter NOT IN ('A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L',
                            'M', 'N', 'O', 'P', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y')
        THEN RAISE EXCEPTION USING message = '$';
        END IF;

        IF lvLetter IN ('A', 'B', 'C')
        THEN RAISE NOTICE '2';
        END IF;

        IF lvLetter IN ('D', 'E', 'F')
        THEN RAISE NOTICE '3';
        END IF;

        IF lvLetter IN ('G', 'H', 'I')
        THEN RAISE NOTICE '4';
        END IF;

        IF lvLetter IN ('J', 'K', 'L')
        THEN RAISE NOTICE '5';
        END IF;

        IF lvLetter IN ('M', 'N', 'O')
        THEN RAISE NOTICE '6';
        END IF;

        IF lvLetter IN ('P', 'R', 'S')
        THEN RAISE NOTICE '7';
        END IF;

        IF lvLetter IN ('T', 'U', 'V')
        THEN RAISE NOTICE '8';
        END IF;

        IF lvLetter IN ('W', 'X', 'Y')
        THEN RAISE NOTICE '9';
        END IF;
        
    EXCEPTION
        WHEN OTHERS THEN
            RAISE NOTICE '%',SQLERRM;
    END $GO$ LANGUAGE plpgsql;

    -----------------------------------------------
--Another possible approach
 DO $GO$
    DECLARE
        lvLetter CHAR(1) := 'M';
    BEGIN
        IF lvLetter NOT IN ('A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L',
                            'M', 'N', 'O', 'P', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y')
        THEN 
            RAISE EXCEPTION USING message = '$';
        END IF;

        IF lvLetter < 'D' THEN
            RAISE NOTICE '2';
        ELSIF lvLetter < 'G' THEN
            RAISE NOTICE '3';
        ELSIF lvLetter < 'J' THEN
            RAISE NOTICE '4';
        ELSIF lvLetter < 'M' THEN
            RAISE NOTICE '5';
        ELSIF lvLetter < 'P' THEN
            RAISE NOTICE '6';
        ELSIF lvLetter < 'T' THEN
            RAISE NOTICE '7';
        ELSIF lvLetter < 'W' THEN
            RAISE NOTICE '8';
        ELSIF lvLetter <= 'Y' THEN
            RAISE NOTICE '9';
        ELSE
            RAISE EXCEPTION USING message = '$';
        END IF;

    EXCEPTION
        WHEN OTHERS THEN
            RAISE NOTICE '%',SQLERRM;
    END;
$GO$ LANGUAGE plpgsql;
