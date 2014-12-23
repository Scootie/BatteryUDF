BatteryUDF
==========
This is an expanded Battery UDF, based on [Yashied's original](http://yashied.ru/ProjectFiles/UDF/Battery.au3). Much of my testing during my time at Tom's Hardware and other ghostwriting projects involve(d) deep analysis of technical mobile platforms: notebooks and tablets; ranging from production, preproduction, prototype, etc... states. However, most of the battery information programs you find on sites like [Download.com](http://www.download.com) are designed for end-users. That's hardly a surprise.

The majority of tech editors, journalists, bloggers, etc... utilize these tools to great effect. The problem is that usually, you're only touching the surface of what is very important information, and you're often limited by the nature of the software. For example, PassMark's battery tool tracks battery life but with a fixed workload imposed by the software. What if I want to test H.264 decoding efficiency, specifically? What about web browsing? What about 2D rendering? Or 3D rendering? Surely Crysis 3 has a different workload than Minecraft. As my needs are wide ranging, the tools I need require flexibility.

From any engineering perspective, it's insufficient to simply know that 70% of battery life is left if you don't know the actual battery capacity. Moreover, the scientific process would require the using the current battery capacity to derive the % with significant digits (i.e. 47231Mah/67000Mah = 70.494029% ) instead of relying on the truncated/rounded capacity percentage provided in Window's system tray icon.

Realistically, for any thorough level of dissection of individual hardware components and the total sum of the platform, you need access to low level information. Yashied's original Battery.au3 UDF addressed most of my needs, as it accesses battery information via Microsoft's WinAPI. 

Yashied's work provided a great foundation, but there were gaps that I felt needed to be addressed. As such, I expanded on his original work to provide additional low-level information concerning the current power state (AC/DC), current battery state (Windows' internal battery flags, i.e. low, critical), seconds left at current discharge rate, current CPU fan state (on, off, speed). All of this code was structured such to be compatible with original goal of accessing data in real-time.

This UDF has been in use a several tools that I built, and has been in use by several editors at the largest PC publication and tech firms. A while back, I shared this code with a few QA engineers at Intel, who I was surprised to have learned were using the good old'e scheduled screencap method to check how much battery life a specific task took up. This provides a solid alternative solution that addresses all the technical needs in QA and testing in general. The information provided is very fine-grained, but need not be. The library provides the framework to access whatever information is in the scope of the investigation.

## License

Copyright Caleb Ku 2014. Distributed under the MIT License. (See accompanying file LICENSE or copy at http://opensource.org/licenses/MIT)
