# dsa2
# assign cookie 455
class Solution {
public:
    int findContentChildren(vector<int>& g, vector<int>& s) 
    {
        int i=0,j=0,count=0;
        sort(g.begin(),g.end());
        sort(s.begin(),s.end());
        while(i<g.size() && j<s.size())
        {
            if(g[i]<=s[j])
            {
                count++;
                i++;
                j++;
            }
            else if(g[i]>s[j])
                j++;
        }
       return count;
    }
};
