#include <stdio.h>
#include <string.h>
#include <stdlib.h>

char **temp;                    //to store sorted elements
void sort(char **ar, int n)     //merge sort on strings
{
        int nl,  nh,  i,  j,  k;
        if ( n <= 1 )
                return;
        nl = n/2;                             //mid calculation
        nh = n - nl;
        sort( ar, nl );                       //passing string array with number of strings as n1(i.e, first half)
        sort( &(ar[nl]), nh );                //passing remaining half from middle to last?
        for(k = i = 0, j = nl; i < nl && j < n; k++)  //merge function
        {
                int l1 = strlen( ar[ i ] );
                int l2 = strlen( ar[ j ] );
                if ( l1 < l2 || ( l1 == l2 && strcmp( ar[i], ar[j] ) < 0) )    //sorting in ascending order
                    temp[ k ] = ar[ i++ ];
                else
                    temp[ k ] = ar[ j++ ];
        }
        while ( i < nl )
            temp[ k++ ] = ar[ i++ ];
        while ( j < n )
            temp[ k++ ] = ar[ j++ ];
        for( i = 0; i < n; i++)       //copying back the sorted array into original array
            ar[ i ] = temp[ i ];
}

int main()
{
        char **strings;         //declaration of string array
        int n, i,  j,  min;
        scanf( "%d", &n );
        strings = ( char ** )malloc( n*sizeof( char * ) );      //allocating memory to n string pointers
        temp = ( char ** )malloc( n*sizeof( char * ) );
        for( i = 0; i < n; i++)
                scanf("%ms", &( strings[ i ] ) );       //%m is used when string size is unknown and memory is allocated dynamically according to the input from user.
        sort( strings, n );                               // passing string array to function sort
        for( i = 0; i < n; i++)                              //printing sorted array
                puts( strings[ i ]);
    return 0;
}
