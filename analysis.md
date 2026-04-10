Programming Assignment Analysis  
EECE 2540  
Justin Glabicki

1\) Highest Inefficiency Ratio  
The city with the highest inefficiency ratio in my results is London, with a ratio of approximately 5.68. This is significantly higher than the typical expected range of \~1.5–3 for well-routed paths, indicating substantial routing inefficiency.  
Looking at submarine cable infrastructure (e.g., via submarinecablemap.com), London is served by numerous transatlantic fiber cables connecting Europe and North America, such as MAREA, AC-1, and others. In theory, this should allow for relatively direct and efficient routing between the U.S. and London. However, the high observed RTT suggests that my traffic did not take a direct transatlantic path. Instead, it was likely routed through multiple intermediate networks or exchange points, possibly due to ISP peering policies, congestion, or suboptimal routing decisions.  
This highlights that even when strong physical infrastructure exists, actual internet routing depends on economic agreements and network policies, not just geography. As a result, packets may take longer, indirect paths that significantly increase latency.

2\) City Closest to Theoretical Minimum  
The city closest to the theoretical minimum RTT is Sydney, with an inefficiency ratio of approximately 1.36, followed closely by Singapore (1.51).  
A ratio close to 1 indicates that the measured RTT is relatively close to the physical limit imposed by the speed of light in fiber. This suggests that routing to Sydney is relatively efficient despite the large geographic distance. The likely reason is that major transoceanic routes (such as transpacific cables) are well-developed and optimized, allowing traffic to follow a relatively direct path with fewer detours.  
This tells us that routing infrastructure along this path is well-optimized, with good peering agreements and relatively direct long-haul fiber routes. It demonstrates that long distance does not necessarily imply inefficiency. What matters more is how direct and well-connected the network path is.

3\) Why Traffic to Lagos Routes Through Europe  
The RTT and inefficiency ratio for Lagos (2.17) suggest moderate inefficiency, and traffic from the U.S. to Lagos is likely routed through Europe rather than directly to West Africa.  
This occurs because Africa’s internet infrastructure is less interconnected internally and globally compared to Europe or North America. Many submarine cables serving West Africa (such as WACS and ACE) connect African countries primarily to European landing points rather than directly to North America. As a result, packets often travel from the U.S. to Europe to West Aftica instead of taking a more direct transatlantic route.  
This routing pattern is driven by limited direct U.S.-West Africa cable capacity, stronger peering and exchange infrastructure in Europe, and the historical development of network connectivity centered around Europe.  
To improve this, more direct submarine cables between North America and West Africa, along with improved regional internet exchange points (IXPs) within Africa, would be needed. Better local interconnection and peering would reduce reliance on European transit and bring RTTs closer to the theoretical minimum.

