using System;
using System.Text;

namespace Assignment_11_George
{
    class Program
    {
        static void getrent(ref int [] apartments, ref int [] rent, int apartmentNumber)
        {
              # Go through list to see if entry matches number from list
              
             for (int i=0; i<4; ++i) // go over every number in the list
                {
                          #if entry matches print results
                          
                    if (apartments[i] == apartmentNumber) // check if it matches
                    {
                        printit(apartmentNumber, ref rent);
                        break; // no need to check any further
                    }
             
            }
        }

        static void printit(int apartmentNumber, ref int[] rent)
        {
              # Create sting builder object and add parts
              
            var output = new StringBuilder();
            output.Append("Rent for apartment # ");
            output.Append(apartmentNumber);
            output.Append(" is $");
           
            # print output
            
            Console.WriteLine(output);
        
        }

        static void Main(string[] args)
        {
            int[] apartments = { 123, 204, 601, 609, 612};
            int[] rent = { 123, 204, 601, 609, 612 };
        

            Console.Write("What is your apartment number? ");
            int apartmentNumber = Convert.ToInt32(Console.ReadLine());
            getrent(ref apartments, ref rent, apartmentNumber);

        }


    }
}
