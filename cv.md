# Erik Sadgalin

#### Contact Info
- telegram: t.me/erictronic
- phone: +7(702)612-71-98

#### Summary
    Computer Science student at CAU. Highly motivated to start career in Software Development. RSS Javascript course is a great opportunity for me to do so.   
	I am planning to find internship after completion of the course, but most importantly gain hard-skills in Javascript and experience of working in a group.   
	I understand that here nobody will babyseat me and I have to work hard and learn fast but I am always ready for new challenges.

#### Skills
    1. Algorithms and Data Structures
    2. Java syntax
    3. basic OOP concepts
    4. C++ (but only used for Algorhitms course I took at my school)

#### Code Example
    below is simple implementation of merge sort. Right now I have no experience in writing industrial code.

```
#include <iostream>
#include <vector>

using namespace std;

template<class T>
vector<T> Merge(vector<T> a, vector<T> b)
{
	vector<T> c;
	
	int i = 0, 
		j = 0;
	
	while (true)
	{
		if (i >= a.size() || j >= b.size()) 
			break;
		if (a[i] < b[j])
		{
			c.push_back(a[i]);
			i++;
		} 
		else 
		{
			c.push_back(b[j]);
			j++;
		}
	}
	while (i < a.size()) c.push_back(a[i++]);
	while (j < b.size()) c.push_back(b[j++]);
	return c;
} 

template<class T>
vector<T> Sort(vector<T> a)
{
	if (a.size() < 2) return a;
	return Merge(Sort(
					   vector<T>(
					              a.begin(), 
					              a.begin() + a.size() / 2
					            )
					  ), 
				 Sort(
				 	   vector<T>(
				 	              a.begin() + a.size() / 2, 
				 	              a.end()
				 	            )
				 	 )
				);
}

int main()
{
	int n;
	cin >> n;
	vector<int> a(n);
	for (int i = 0; i < n; i++)
		cin >> a[i];
	a = Sort(a);
	for (int i = 0; i < n; i++)
		cout << a[i] << ' ';
}
```
#### Experience
    No real industrial code experience besides Javascript Course from HTMLacademy which I started recently, homeworks and university project  
	to which I did small contribution and I do not want to take credit for.
