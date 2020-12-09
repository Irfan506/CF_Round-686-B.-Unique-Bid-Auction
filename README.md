# CF_Round-686-B.-Unique-Bid-Auction
using System;
using System.Linq;
namespace unique_bid_auction
{
    class Program
    {
        static void Main(string[] args)
        {
            int t = Convert.ToInt32(Console.ReadLine());
            while(t!=0)
            {
                t--;
                int n = Convert.ToInt32(Console.ReadLine());
                int ans = -1;
                int[] index = new int[n+1];
                int[] brr = new int[n + 1];
                int[] num = Console.ReadLine().Split(' ').Select(x => int.Parse(x)).ToArray();
                for (int i = 0; i< n; i++)
                {
                    brr[num[i]]++;
                    index[num[i]] = i;
                }
                for (int i = 1; i <= n; i++)
                {
                    if(brr[i]==1)
                    {
                        ans = index[i]+1;
                        break;
                    }
                }
                Console.WriteLine(ans);
            }
        }
    }
}
