# ziko
#include <iostream>

using namespace::std;
#define size 5


struct Stack
{

	int list[size];
	int counter ;
};




bool push(Stack* arr, int data)
	{
		if (arr->counter<size-1)
		{		
			arr->counter++;
			arr->list[arr->counter] = data;
			return true;
		}
		//return false;
	}

void pop(Stack* arr)
	{
	
			arr->counter--;	
	}

void initial(Stack* arr)
{
	arr->counter=-1;
}

void Print(Stack* arr)
	{
		cout << "{";
		for (int i = 0; i <= arr->counter; i++)
		{
			cout << arr->list[i] << " ";
		}
		cout << "}\n";
	}


int main(){
	
 Stack arr;

 initial(&arr);
 
 
  push(&arr,2);
  push(&arr,3);
  push(&arr,4);
  push(&arr,5);
  push(&arr,7);
 pop(&arr); 
  //cout<<arr.list[0]<<endl;
  //cout<<arr.list[1]<<endl;
  //cout<<arr.list[2]<<endl;
  //cout<<arr.list[3]<<endl;
  //cout<<arr.list[4]<<endl;	
  
  Print(&arr);
	
	
}
