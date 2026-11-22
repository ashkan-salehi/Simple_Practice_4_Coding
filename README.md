#  **Some notes to share:**

##  number 1
For input(), using list comprehension is the idea that I had initially but I finalized it by using AI.
cf1=[float(x) for x in input("enter your list: ").split()]

##  number 2
Sometimes I tend to use multiple if s rather than if, elif and else. I initially did this here but it is not an efficient code at all 

a, b = compare(cf1, cf2, rate)
if a > b:
  print(f"for rate {rate} , the NPV1 is {a: .2f}.")
if b > a:
  print(f"for rate {rate} , the NPV2 is {b: .2f}.")
if a==b:
  print(f"for rate {rate} , the NPV1 and NPV2 are equal.")

Vs.

a, b = compare(cf1, cf2, rate)
if a > b:
  print(f"for rate {rate} , the NPV1 is {a: .2f}.")
elif b > a:
  print(f"for rate {rate} , the NPV2 is {b: .2f}.")
else:
  print(f"for rate {rate} , the NPV1 and NPV2 are equal.")


##  number 3
Honestly, it is not necessary to use “warning”. I used it just for the sake of practice. 
if len(cf1) != len(cf2):
        warnings.warn(
            "The two lists have different lengths. This might cause unexpected behavior!",
            UserWarning
        )
