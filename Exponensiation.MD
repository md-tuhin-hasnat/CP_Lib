# Different type of Exponensiation used in competitve programmin

## Binary Exponensiation

```c++
ll bin_exp(ll x,ll y){
  ll ans = 1;
  while(y > 0){
    if(y&1) ans = (ans*x);
    x = (x*x);
    y >>=1;
  }
  return ans;
}
```
## Modular Exponensiation

```c++
ll mod_exp(ll x,ll y,ll mod){
  ll ans = 1;
  while(y > 0){
    if(y&1) ans = (ans*x)%mod;
    x = (x*x)%mod;
    y >>=1;
  }
  return ans;
}
```
We can find inverse modulo of a number **a** using **Modular Exponensiation** if the modulo is a **prime number**,
$${
a^{p-2} = a^{-1}&nbsp{mod}&nbsp{p}
}$$
To find the above expression, we can simply use,
```c++
long long invers_modulo_of_a = mod_exp(a,mod-2,mod);
```
