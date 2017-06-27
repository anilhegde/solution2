import java.util.*;

class Word{
String s;
int ind;
 
}
 
class solution2
{
void getArr(String[] arr,int n){
Word[] word=new Word[n];
for(int i=0;i<n;i++){
word[i]=new Word();
String a=arr[i];
char[] A=a.toCharArray();
Arrays.sort(A);
a=(String.valueOf(A));
word[i].ind=i;
word[i].s=a;
 
}
Arrays.sort(word,new mycomparator());
for(int i=0;i<n;i++){
int index=word[i].ind;
System.out.print(arr[index]+" ");
 
}
 
 
}
 
 
 
 
public static void main (String[] args) throws java.lang.Exception
{
solution2 k = new solution2();
String[] arr={ "listen", "pot", "part", "opt", "trap", "silent", "top", "this", "hello", "hits", "what", "shit"};
k.getArr(arr,arr.length);
  
}
}
class mycomparator implements Comparator<Word>{
 
public int compare(Word a,Word b){
return (a.s.compareTo(b.s)>0)?1:-1;
}
}
