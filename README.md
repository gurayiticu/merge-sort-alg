# merge-sort-alg
public int [] mergesort(int [] m)
   {

     int x=0;
     int y=0;
     int middle=m.length/2;
     int left[] =new int [middle];
     int right[] =new int [middle];
     int result[] =new int[(m.length)];

     if(m.length<= 1){
       return m;
     }

     for(int i=0; i<middle; i++)
     {
       left[x]=m[i];
       x++;
     }
     for(int i=middle; i<m.length; i++)
     {
       right[y]=m[i];
       y++;
     }
     left=mergesort(left);
     right=mergesort(right);
     result=merge(left,right);
     return result;
   }
