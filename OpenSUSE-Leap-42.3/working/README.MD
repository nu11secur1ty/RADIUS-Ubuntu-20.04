# by OpenSuse and nu11secur1ty S.A.I.E
# Setting Up a FreeRADIUS Serve

The RADIUS (Remote Authentication Dial-In User Service) protocol has long been a standard service for manage network access. It performs authentication, authorization, and accounting (AAA) protocol for very large businesses such as Internet service providers and cellular network providers, and is also popular for small networks. It authenticates users and devices, authorizes those users and devices for certain network services, and tracks use of services for billing and auditing. You don't have to use all three of the AAA protocols, but only the ones you need. For example, you may not need accounting but only client authentication, or perhaps all you want is accounting, and client authorization is managed by something else.

It is extremely efficient and manages thousands of requests on modest hardware. Of course it works for all network protocols and not just dialup, but the name remains the same.

RADIUS operates in a distributed architecture, sitting separately from the Network Access Server (NAS). User access data is stored on a central RADIUS server that is available to multiple NAS. The NAS provide the physical access to the network, such as a managed Ethernet switch, or wireless access point.

FreeRADIUS is the open source RADIUS implementation, and is the most widely-used RADIUS server. In this chapter you will learn how to install and test a FreeRADIUS server. Because of the numerous possible use cases, after your initial setup is working correctly your next stop is the official documentation, which is detailed and thorough (see https://freeradius.org/documentation/).
