# hw

#question 1
a) the graph has 5 verticies
b) 
a->c->b 6*8
a->d->b 11*7
a->e->b 1*11
a->a->b 9*3
a->b->b 3*15
      + = 208

# question 2
ram: 4915200000 k 
float = 4 bytes

4915200000 / 2 <- float * float = 2457600000
2457600000 / 4 <- size of float = 614400000

therefore the largest N * N float array can be 614400 * 614400

# question 3
To do that would be as simple as zeroing out sections that aren't inside the tile range

so that way when the tile is over flow it just is zeroed out since it isn't in the block range
example
1 0 <- 2 colums in range 0 0 <- 2 colums out of range just zero them
0 1                      0 0

# question 4
a) answer:
 1.000   0.000   0.000   0.000   0.000   0.000   0.000   0.000
  2.000   1.000   0.000   0.000   0.000   0.000   0.000   0.000
  4.000   4.000   1.000   0.000   0.000   0.000   0.000   0.000
  8.000  12.000   6.000   1.000   0.000   0.000   0.000   0.000
 16.000  32.000  24.000   8.000   1.000   0.000   0.000   0.000
 32.000  80.000  80.000  40.000  10.000   1.000   0.000   0.000
 64.000 192.000 240.000 160.000  60.000  12.000   1.000   0.000
128.000 448.000 672.000 560.000 280.000  84.000  14.000   1.000
b)
check code
c)
ram: 4915200 kB 
int = 2 bytes

4915200000 / 2 = 2457600000
2457600000 / 2 <-size of int= 1228800000
therefore 1228800000 * 1228800000 int array
d)
ram: 4915200 kB 
int = 2 bytes

4915200000 / 2 = 2457600000
2457600000 / 8 <-size of double= 307200000
therefore 307200000 * 307200000 double array

I'm not sure  I understand, According to c data type sizes a double is 8b therefore there would be a smaller size of doubles allowed
according to my calculations the max size would be: a 307200000 * 307200000 matrix  but there would be problems since when creating it 
ram runs out because there are more variables other than just the grid .

also limited to 2,147,483,647 since that is the max int size