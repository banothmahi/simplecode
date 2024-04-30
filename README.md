class Solution {
  public:
    
    int firstRepeated(int arr[], int n) {
        unordered_map<int,int>freq;
        for(int i=0;i<n;i++)
        {
            freq[arr[i]]++;
        }
        for(int i=0;i<n;i++)
        {
            if(freq[arr[i]]>=1)
            {
                return freq[arr[i+1]];
            }
            else
            {
                return freq[arr[i-1]];
            }
        }
        // code here
    }
};
