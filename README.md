This small notebook compares a Constant Product Automated Market Maker (CPAMM) using Uniswap v1 math to one using Uniswap [v3](https://uniswap.org/whitepaper-v3.pdf) math. (The v3 [whitepaper](https://uniswap.org/whitepaper-v3.pdf) will explain both)  
  
The v1 AMM is simple enough, the product of the quantities of each price remains constant with each trade. Liquidity is added to the pool in an even ratio always.
The v3 AMM is more involved, ticks are used to demark tiny discrete price values between which concentrated liquidity positions can be taken. The AMM will then trade like a v1 AMM but with a higher effective liquidity while the price is in the range of a position, allowing it to reduce slippage.  
  
Test:
Each AMM is provided with 10000 of assets A and B, but the v3 AMM has its price range restricted to [0.5,1.5] instead of v1's default [0,inf). 500 of asset B is then traded with the pool.
Slippage is noticeably less on the v3 AMM due to concentrated liquidity.  
![image](https://github.com/user-attachments/assets/b626f8c4-3e71-4b35-a48b-8cece5bfbc25)  
![image](https://github.com/user-attachments/assets/a9e52903-666d-4b9b-9c14-59a36465ecf1)  
  
Feel free to adopt the code and play around with the inputs to each AMM
