## Abstract 
Caches are like a faster and more efficient version of memory that help speed up computer operations. However, the best way to set up a cache depends on how a specific program uses memory. When switching between different tasks, the cache needs to be cleared and refilled with new data, which takes time and energy.

To make caches work better, researchers have come up with different techniques. One idea is called cache partitioning, where the cache is divided into smaller sections. When a program is running, it can choose the most appropriate section of the cache to use by following special instructions. This approach reduces the interference between different programs' cache data and makes switching between tasks faster and more efficient. Ultimately, this helps improve overall performance and reduces the time and energy wasted during context switches.

----
## Related works
Different computer programs and the way they access memory can affect the performance and power usage of the system they run on. To improve performance, researchers have come up with various methods to optimize a component called the cache, which stores frequently used data.

Some methods focus on specific aspects of the cache, while others consider all the important factors. For example, A.Patel et al. (2006) suggest a method that reduces the number of memory access conflicts in a specific type of cache by selecting certain bits of the memory address. This method improves performance by making better use of the cache.

Another method proposed by Albonsei et al. (1999) allows for selective activation of cache portions based on demand. When the system requires high performance, the entire cache is utilized, but when the demand is lower, only a portion of the cache is activated. This approach saves power by activating only what is needed.

In some cases, the cache is not fully utilized, leading to decreased performance. Rolan et al. (2009) suggest a method called "Set balancing" that redistributes data within the cache sets to alleviate this problem. By moving data from sets with high miss rates to sets with unused space, performance can be improved.

Zhang et al. (2003) propose a cache architecture that can be configured through software. By adjusting a few settings, the cache can be set up as either direct-mapped or set-associative, utilizing its full capacity while still providing flexibility.

Gordon-Ross et al. (2007) introduce hardware modules that predict the best cache configuration for a program in real-time. By analyzing the program's memory access patterns, the cache is adjusted on the fly, resulting in improved performance and reduced energy usage.

Zhang et al. (2004) suggest a self-tuning cache architecture that dynamically adjusts its configuration based on program behavior. By continuously monitoring the program's cache misses, the cache parameters are adapted to minimize performance bottlenecks.

Building on this idea, Gordon-Ross and Vahid (2007) propose a cache architecture that can be reconfigured dynamically based on the program's behavior. By profiling the program and identifying frequently accessed memory blocks, the cache is optimized to improve overall performance.

In summary, these researchers have proposed various methods and techniques to optimize cache configurations in embedded systems. Their approaches aim to enhance performance, reduce power consumption, and improve the utilization of the cache based on the specific requirements of different programs.

---

## Methodology
When we switch between different tasks on a computer, it takes time and energy to clear and reload the cache. This can slow down the switching process. To solve this problem, we propose a switchable cache system.

In our solution, we have multiple cache banks, each with different cache settings. These settings are determined when the system is designed and optimized for specific programs. Users can choose the best cache configuration for a particular program using a special instruction added to the system. These configurations are already pre-established during the design stage.

If there are more programs than available cache banks or for general cases, we have a special hardware unit that handles this situation. When a task switch happens, this hardware selects the cache bank used by the previous task. This way, we don't have to clear the cache and reload the data, saving time and reducing the need for memory access.

To implement this cache bank system, we built upon a previous solution called Switchable Cache developed by Nawinne et al. in 2016, and made further improvements to meet our specific requirements.