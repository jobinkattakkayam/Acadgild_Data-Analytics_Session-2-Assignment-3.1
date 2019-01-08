# Acadgild_Data-Analytics_Session-3-Assignment-3.1

The R-script for the given problem is as follows:

# Make a lower triangular matrix (zeroes in upper right corner)

m=8; n=8;

ctr=0;                   # used to count the assignment

x_mat = matrix(0,m,n)    # create a 8 x 8 matrix with zeroes 

x_mat

for(i in 1:m) 

{

  for(j in 1:n) 
  
  {   
  
    if(i==j)              # if the indexes are equal
    
    { 
    
      break;
      
    } 
    
    else                  # if the indexes are not equal
    
    {
    
      x_mat[i,j] = i+j    # assign the values only when i<>j
      
      ctr=ctr+1
      
    }
    
  }
  
  print(i+j) 
  
}

print(ctr)                # print how many matrix cells were assigned

x_mat

    Here m x n matrix of zeroes is created using matrix(0,m,n); 
    
    where m=8 and n=8 Hence, 8 X 8 lower triangular matrix is created whose elements below the main diagonal are non-zero, 
    
    the others are left untouched to their initialized zero value.
    
When the indexes are equal ( i = = j ), a break is executed and the innermost loop is interrupted with a direct jump to the instruction following the inner loop, which is a print; then control gets to the outer for condition (over the rows, index i), which is evaluated again.

If the indexes differ (I is not equal to j), the assignment is performed and the counter (ctr ) is incremented by 1.
The program prints the counter ctr = 28 (in given sample matrix of order 8 X 8 ), which contains the number of elements that were assigned.

The final value of x_mat gives the lower triangular matrix.

