 # MVC_FBLab

FizzBuzz is a very simple programming task, used in software developer job interviews, to determine whether the job candidate can actually write code. 

  - It was invented by Imran Ghory, and popularized by Jeff Atwood.
  - Write a program that prints the numbers from 1 to 100
  - For multiples of three print “Fizz” instead of the number and for the multiples of five print “Buzz”. For numbers which are multiples of both three and five print “FizzBuzz”.

# Code - HomeController 
 - Code shown is for the code used to add the "solve" View
 - TThe 2nd solve is for the program to run it / give solution
```sh
[HttpGet]
        public IActionResult Solve()
        {
            ViewData["Solution"] = "";
            return View();
        }
        [HttpPost]
        public IActionResult Solve(int fizz, int buzz)
        {
            var returnValue = "";
            for (var i = 1; i <= 100; i++)
            {
                if (i % fizz == 0 && i % buzz == 0)
                {
                    returnValue += "FizzBuzz ";
                } 
                else if (i % fizz == 0)
                {
                    returnValue += "Fizz ";
                }
                else if (i % buzz == 0)
                {
                    returnValue += "Buzz ";
                }
                else
                {
                    returnValue += $"{i} ";
                }

            }
            ViewData["Solution"] = returnValue;
            return View();
        }
```


 
