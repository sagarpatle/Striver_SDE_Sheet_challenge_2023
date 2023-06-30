#include <bits/stdc++.h> 

/************************************************************

 

    Following is the TreeNode class structure

 

    template <typename T>

    class TreeNode {

       public:

        T data;

        TreeNode<T> *left;

        TreeNode<T> *right;

 

        TreeNode(T data) {

            this->data = data;

            left = NULL;

            right = NULL;

        }

    };

 

************************************************************/

 

class BSTiterator

{   public:

    vector<TreeNode<int>*>arr;

    int i;

    BSTiterator(TreeNode<int> *root)

    {

        // write your code here

        x(root,arr);

        i=0;

        

        

        

    }

    void x(TreeNode<int>*root,vector<TreeNode<int>*>&arr){

        if(root==NULL){

            return;

        }

        x(root->left,arr);

        arr.push_back(root);

        i++;

        x(root->right,arr);

    }

 

    int next()

    {

        // write your code here

        if(i<arr.size()){

 

            return arr[i++]->data;

        }

        

    }

 

    bool hasNext()

    {

        // write your code here

        if(i<arr.size()){

            return true;

        }

        return false;

    }

};

 

/*

    Your BSTIterator object will be instantiated and called as such:

    BSTIterator iterator(root);

    while(iterator.hasNext())

    {

       print(iterator.next());

    }

*/

