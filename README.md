# matchspec
string encoded_String(string str)
{
    unordered_map<char,int>mp;
   int j=1;
   string ans;
   for(auto i: str)
   {
       if(mp.find(i)==mp.end())
       {
           mp[i]=j++;
       }
       ans+=to_string(mp[i]);
   }
   return ans;
}
vector<string> findMatchedWords(vector<string> dict,string pattern)
{
       //Your code here
     vector<string>ans;
     int n=dict.size();
     string c=encoded_String(pattern);
     for(int i=0;i<n;i++){
         if(encoded_String(dict[i])==c){
             ans.push_back(dict[i]);
         }
     }
       return ans;
}
