using namespace std;
#include <iostream>
#include <vector>

bool isSubset(vector<int> & a, vector<int> & b) {
  
    // Iterate over each element in the second array
  int m=a.size(),n=b.size();
    for (int i = 0; i < n; i++) {
       // bool found = false;
      
                                                // Check if the element exists in the first array
                                                // we can use a bool variable found . its ok;
        for (int j = 0; j < m; j++) {
            if (b[i] == a[j]) {
                //found = true;
                //break;
                return true;
                break;
            }
        }
      
        // If any element is not found, return false
        //if (found==false) 
        ;return false;
    }
  
    // If all elements are found, return true
    return true;
}

int main() {
    vector<int> a = {1, 19, 13, 21, 3, 7,11};
    vector<int> b = {11, 3, 7, 1};
  
    if (isSubset(a, b)) {
        cout << "true" << endl;
    } else {
        cout << "false" << endl;
    }

    return 0;
}
