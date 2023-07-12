# Gas_Challenge
In the Gas Challenge contract,several updates to optimize gas consumption was made. First, I changed the array to a fixed-size array to reduce gas costs. Next, I cached the sum of the array as a private state variable to avoid recomputing it. I also optimized the notOptimizedFunction by setting the array elements and the cached sum directly to zero. Additionally, I used the unchecked block in the optimizedFunction to skip overflow checks. Lastly, I modified the visibility of the getSumOfArray function to public to access it in the test. These optimizations minimize gas costs and improve the efficiency of the contract execution.

# Test_Challenge
In the test for the Gas Challenge contract, we have a test case named "Check Sum Of Array". The purpose of this test is to ensure that after running the gas optimized function, the sum of the array is indeed 0.

To perform the test, I first call the `optimizedFunction` on the `gas_contract` instance. This function sets all elements of the `numbers` array to 0 and updates the cached sum to 0 as well. 

Then, I retrieve the sum of the array by calling the `getSumOfArray` function on the `gas_contract` instance. I store the returned sum in the `sum` variable.

Finally, using the `expect` assertion from the Chai library, I compare the value of `sum` with the expected value of 0. If the sum is equal to 0, the test case passes; otherwise, it fails.

This test ensures that the gas optimized function is correctly updating the array elements and the sum, resulting in a sum of 0 as expected.
