# Leak report


_The only leak was located in the function/method "is_cleaned." Upon first test to see if the issue had problems, it stated the leak was located in either "strip", "is_cleaned" or "main". "Main" calls "is_cleaned" and "strip" allocates memory for any char. Therefore, it was clear that it needed to be in "is_cleaned". According to the example on the "README.md" we had to free it before returning. So placing "free(cleaned);" right before return, frees the memory._

