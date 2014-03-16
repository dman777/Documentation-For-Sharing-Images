.. _basic_concepts:
***************************
Quickstart and Fundamentals
***************************

Sharing is not duplicating
--------------------------
Image sharing is exactly what it sounds....sharing a image between two Rackspace accounts. It is not copying a image and having two of of the same images(although this is possible and discussed later). When you share a image with another person, you give them a reference to your image. Think of it as you are givng the other person a roadmap to where their account can find your image to use.

Think ahead
-----------
.. note:: Since the writing of this article, image transferring(not sharing) is now available. Please see `Transferring Images Between Regions of the Rackspace Open Cloud <http://www.rackspace.com/knowledge_center/article/transferring-images-between-regions-of-the-rackspace-open-cloud>`_ for documentation. This is a fantastic new feature and adds great flexibility. However, it is not the same as sharing a image and is not included in this documentation since it is out of this context. If you plan to share images on a repeated basis, you may still want to take in account the points below. 

Images can not be shared(please see note above) across datacenters. For instance, if you have a image in the Dallas datacenter you can only share it with accounts in the Dallas datacenter. This makes good sense - you would not want to stream a 40GB image across datacenters. This would take a very long time to stream such a image. In addition, the probability of corruption is high due to typical internet congestion. The key point is this: Plan ahead on which datacenter you will choose to do your image sharing. As rule of thumb, it is best to pick the datacenter closest to you. However, the difference in speed across the datacenters from where you are are only milliseconds and insignificant to the human being.  

Producer? What? I am the owner of the image
-------------------------------------------
Original documentation refers to the owner of the image as the "producer". If you are the owner of the image you want to share, think of yourself as "producing the image". 

Consumer? What? I want to use Jill's image and build a server off of it
-----------------------------------------------------------------------
The consumer will be the person who is using a image that is being shared with them.

Consumers are referred to by their account id
----------------------------------------------
Let's say that I, Darin, want to share my image ``af1234c9-6d07-5f1f-b642-01d9df26ed51`` with Jill. Jill will let me know her account number which is ``1234567``. I will add consumer ``1234567`` to my custom build Ubuntu image ``af1234c9-6d07-5f1f-b642-01d9df26ed51`` so it will be available to Jill's account.

Windows images are non transferable
------------------------------------
Windows images are under a licenese that prohibits them being transferable.

I'm ready to start sharing images! 
----------------------------------
With this much information, you can now go to `www.cloudshareimage.com <https://cloudshareimage.com>`_ and share images. On the site you can go two ways:

1)  You can make use of ``Share Image All In One Step`` if you have both the producer's and consumer's account api keys

.. note:: Step 2 is ideal if the Producer and Consumer do not share their api keys

2)  Do each step individually-  Use ``Producer Operation-> Add Member`` to add a member your image. For the consumer, he/she/you will want to use ``Consumer Operations-> Set status of image`` to ``Accept``. This is will allow the shared image to be available in the consumer's account.  


