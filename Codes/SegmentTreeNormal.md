# Segment Tree Normal

There should be an array named **tree[N*4]**

## Segment Tree Building

```cpp
  void build_tree(int node, vector<int> &v, int rengeLeft, int rengeRight){
    if(rengeLeft==rengeRight){
      tree[node] = v[rengeLeft];
      return;
    }
    ll leftNode = node*2, rightNode = leftNode+1;
    int rengeMid = (rengeLeft+rengeRight)/2;
    build_tree(leftNode,v,rengeLeft,rengeMid); 
    build_tree(rightNode,v,rengeMid+1,rengeRight);
    tree[node] = tree[leftNode]+tree[rightNode];
  }
```

## Segment Tree Update
```cpp
  void update_tree(int node, vector<int> &v, int rengeLeft, int rengeRight, int point, int value){
    if(rengeLeft == point && rengeRight == point){
      tree[node] = value;
      return;
    }
    else if(rengeLeft > point || rengeRight < point) return;
    int rengeMid = (rengeLeft+rengeRight)/2;
    int leftNode = node*2, rightNode = leftNode+1;
    update_tree(leftNode,v,rengeLeft,rengeMid,point,value);
    update_tree(rightNode,v,rengeMid+1,rengeRight,point,value);
    tree[node] = tree[leftNode]+tree[rightNode];
  }
```
## Segment Tree Query

```cpp
  void update_tree(int node, vector<int> &v, int rengeLeft, int rengeRight, int point, int value){
    if(rengeLeft == point && rengeRight == point){
      tree[node] = value;
      return;
    }
    else if(rengeLeft > point || rengeRight < point) return;
    int rengeMid = (rengeLeft+rengeRight)/2;
    int leftNode = node*2, rightNode = leftNode+1;
    update_tree(leftNode,v,rengeLeft,rengeMid,point,value);
    update_tree(rightNode,v,rengeMid+1,rengeRight,point,value);
    tree[node] = tree[leftNode]+tree[rightNode];
  }
```
