void helper(int i, vector<int> arr, int n, int k, vector<vector<int>> &ans, vector<int> &v){
    if(i == n){
        if(k == 0){
            ans.push_back(v);
        }
        return;
    }
    v.push_back(arr[i]);
    helper(i+1, arr, n, k - arr[i], ans, v);
    v.pop_back();
    helper(i+1, arr, n, k, ans, v);
}

vector<vector<int>> findSubsetsThatSumToK(vector<int> arr, int n, int k)
{
    int i = 0;
    vector<vector<int>> ans;
    vector<int> v;
    helper(i, arr, n, k, ans, v);
    return ans;
}
