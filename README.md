void doInsertSort(int[] a){
  for(int i=1;i<a.length;i++){
    int temp = a[i];
    int j = i-1;
    while(j>=0 && a[j]>temp){
      a[j+1]=a[j];
      j--;
    }
    a[++j]=temp;
  }
}

void doMpSort(int[] a){
  for(int i=0;i<a.length-1&&flag;i++){
    boolean flag = false;
    for(int j=a.length-1;j>i;j--){
      if(a[j]<a[j-1]){
        int temp = a[j];
        a[j] = a[j-1];
        a[j-1] = temp;     
        flag = true;
      }
    }
  }
}

void doSelectSort(){
  for(int i=0;i<a.length-1;i++){
    int min = i;
    for(int j=i+1;j<a.length;j++){
      if(a[min] > a[j]){
        min = j;
      }
    }
    if(min != i){
      int temp = a[min];
      a[min] = a[i];
      a[i] = temp;
    }
  }
}
