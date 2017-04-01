# hw

# plot     
size	share time(ms)	no share(ms)
1000	710	720
2000	820	920
3000	1300	1450
4000	1310	2290
5000	2120	4190
6000	2980	6000
7000	4450	9810
8000	5990	13300
9000	8540	19910
10000	10870	25250

chart is in "chart.png"

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
ram: 4915200000 bytes 
float = 4 bytes

4915200000 / 3 <- 3 matrices are needed A * B = C = 1638400000 so each matrix has at max that many bytes
1638400000 / 4 <- size of float = 409600000
sqrt(409600000) = 20238

therefore the largest N * N float array can be 20238 * 20238

# question 3
To do that would be as simple as zeroing out sections that aren't inside the tile range, You can do that by just testing
the blockId * blockDim + threadId to find how far it should go. You would have to do this for both the y and x since
the row might go off but the column could still fit

so that way when the tile is over flow it just is zeroed out since it isn't in the block range
example
1 0 <- 2 colums in range 0 0 <- 2 colums out of range just zero them
0 1                      0 0

# question 4
a) answer:
Identity Matrix
b)
check code
c)
ram: 4915200 kB 
int = 2 bytes

4915200000 / 3 = 1638400000
1638400000 / 2 <-size of int = 819200000
sqrt(819200000) = 28621
therefore there can be 3 28621 * 28621 int array
d)
ram: 4915200 kB 
int = 2 bytes

4915200000 / 3 = 1638400000
1638400000 / 8 = 204800000
sqrt(204800000) = 14310
therefore 14310 * 14310 double array

I'm not sure  I understand, According to c data type sizes a double is 8b therefore there would be a smaller size of doubles allowed
according to my calculations the max size would be: a 14310 * 14310 matrix  but there would be problems since when creating it 
ram runs out because there are more variables other than just the grid .

also limited to 2,147,483,647 since that is the max int size