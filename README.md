# PandaScotlandFlag
using System;
					
public class Program
{
	public static void Main()
	{
		 	int n = int.Parse(Console.ReadLine());
            int a = 0;
			bool DEBUG = false; //true to print debug output; false to skip it

            //Console.WriteLine("A{0}B", new string('#', n - 2));
		
			string alpha = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
			for (int i = 0; i < n; i++)
			{  
    			
				while(a < (n-1)/2)
				{				
					Console.WriteLine("{0}{1}{2}{3}{0}", new string('~', a), alpha[i%26], new string('#', (n-2)-2*a), alpha[(i+1)%26]); 
					i+=2;
					a++;
				}
				
					
				if (a == (n-1)/2)
				{
					Console.WriteLine("{0}{1}{0}", new string('-', (n-1)/2), alpha[i%26]); 
				i++;
				}
				
					
				while(a > 0)
				{	
					a--;			
						
					if (DEBUG) //debug
							Console.WriteLine("lower i:{0} a:{1} (n-2)-2*a:{2}", i, a, (n-2)-2*a);
					
					Console.WriteLine("{0}{1}{2}{3}{0}", new string('~', a), alpha[i%26], new string('#', (n-2)-2*a), alpha[(i+1)%26]);
					i+=2;
					
				}
				
				
			}
					
		}

}
