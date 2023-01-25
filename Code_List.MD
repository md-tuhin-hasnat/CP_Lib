# Some Useful code I use in competitve programming
1. <details>
      <summary>Binary Exponenciation</summary>
  
      ```C++
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
  </details>
  
2. <details>
      <summary>Moduler Exponenciation</summary>
  
      ```C++
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
  </details>
