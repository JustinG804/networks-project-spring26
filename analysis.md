Programming Assignment Analysis  
EECE 2540  
Justin Glabicki



1\) Highest Inefficiency Ratio  
The city with the highest inefficiency ratio in my results is Sendai, with a ratio of approximately 14.68, followed closely by New Delhi (14.11) and Seoul (13.86). These values are far above the typical range of \~1.5–3, indicating extreme inefficiency.

Unlike earlier measurements using Google endpoints, these results come from university websites, which are not optimized for low-latency global access. While Japan and South Korea have strong submarine cable connectivity (transpacific cables linking Asia and North America), the high RTTs suggest that the delay is not primarily due to physical distance or cable routing. Instead, it is likely caused by server-side processing delays, congestion, or limited optimization of these institutional web servers.

This demonstrates that RTT measurements using HTTP requests include not only propagation delay through fiber but also application-layer delays, such as server response time. As a result, endpoints that are not optimized for performance can produce extremely high inefficiency ratios, even if the underlying network path is relatively direct.



2\) City Closest to Theoretical Minimum  
The city closest to the theoretical minimum RTT is Singapore, with an inefficiency ratio of approximately 1.21, followed by Sydney (1.23) and Mumbai (1.48).

A ratio close to 1 indicates that the measured RTT is relatively close to the physical limit imposed by the speed of light in fiber. This suggests that routing to these locations is highly efficient despite the large geographic distance. The likely reason is that these routes rely on well-developed transoceanic fiber infrastructure, such as transpacific and inter-Asia cable systems, combined with strong peering and routing optimization.

This result shows that long-distance communication can still be efficient if the network path is direct and well-connected. It reinforces that network topology and routing efficiency matter more than raw distance alone.



3\) Why Traffic to Lagos Routes Through Europe  
The RTT and inefficiency ratio for Lagos (\~2.0) suggest moderate inefficiency, and traffic from the U.S. to Lagos is likely routed through Europe rather than directly to West Africa.

This occurs because Africa’s internet infrastructure is less interconnected globally compared to Europe or North America. Many submarine cables serving West Africa (such as WACS and ACE) primarily connect African countries to European landing points rather than directly to North America. As a result, packets often travel:

U.S. -> Europe -> West Africa

instead of taking a more direct transatlantic route.

This routing pattern is driven by limited U.S.-West Africa cable capacity, stronger peering and exchange infrastructure in Europe, and historical development of global network connectivity centered around Europe.

To improve this, more direct submarine cables between North America and West Africa, along with stronger regional Internet Exchange Points (IXPs) within Africa, would be needed. These changes would reduce reliance on European transit and bring RTTs closer to the theoretical minimum.

