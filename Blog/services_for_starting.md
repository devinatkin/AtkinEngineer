[Resume](resume_page.md) [Projects](projects.md), [Blog](blog.md)

# Services for Starting 
So you're starting a new business and want to setup your IT services. There are a lot of different things you'll need and a lot of different ways to set them up. Here are a few items to get yourself started. I'll try and keep this up to date as I think of more items that may be relevant to staritng a small business. So far Email Services.

## Email Accounts
Using @gmail looks tacky, at least in my opinion. It is at least not as bad as using an ISP provided address like @telus or @shaw (Goodness why are those even offered). Services abound to have your own custom domain email address.

- Google Workspace ($7.80 - $23.40 CAD per Month). I personally have a middling plan in order to get more pooled storage. This may appeal if your a fan of other google services. I was initially drawn into this service as I liked the ecosystem, Google Domains for a registrar, Google Workspace for email, Google Cloud for computing. 
- Proton Email ($0 - $12.99 USD per Month). So for the free you just get an @proton mail address, which isn't perfect, but it has a step up on the other addresses because among a certain crowd proton mail is revered for being great for privacy. But with a paid plan you can add your own custom domain and get a bunch of features convenient for businesses, multiple addresses, vpn, and a password manager, sharable with up to 10 other people. Honestly a great price for the service.
- AWS Workmail ($4 USD per month). It's cheap and associated with your AWS account. That plus the ability to add amazon's equivalent of google docs makes it a good way to add items piece meal. It plays nicely with other amazon services which can make it a good option for startups not wanting a lot of management overhead jumping between platforms. 
- Zoho Mail (€0.90 - €3.60 per month). Custom domains, and super cheap. Not a lot of features, especially at the lower end, but honestly amazing value for money. For the higher end you can even white label the mail so that it matches your company branding. 
- Alimail ($13.50 per month for 3 users). If you don't mind the association with Alibaba, and with good cost scaling ($135 per year) it's a reasonable offer when you need multiple accounts. 
- Microsoft 365 Business ($8.10 - $29.80 per month). If you're already locked into using Word, Excel, Powerpoint and the like then you might want to look at a business microsoft account. Plus that should play nicely with Azure cloud I'm sure, which as another major cloud provider has a certain value to it. 

I haven't tried the majority of these options, but they are all ones that look quite good on paper and have the backing of a larger company. If you have specific data needs or peripheral services it'll change what makes the most sense; however, barring VERY strict data requirements don't go self-hosted. It's far too much trouble to manage the service on your own, and far too easy to accident yourself onto a black list. Don't get me wrong there are open source options for running your own mail server, but you're going to want to have an IT department of your own to handle any complications that may come of it. Even large organizations like Universities know it's cheaper and easier to just let someone who specializes in it handle the job. 

## Cloud Services 
You need all sorts of Cloud computers. 

- Alibaba Cloud
- Azure Cloud
- Amazon Webservices
- Google Cloud
- IBM Cloud
- Digital Ocean
- Oracle Cloud

There are a lot of different cloud providers out there. Each with different flavors and different levels of hassle. Some resellers that wrap the larger cloud providers in easier to use services, others that have their own servers. If all you need is computers, then pick a service with a data center near your customer base and load up a virtual machine that can handle what you need. If you need something specific, then, honestly no you don't. If you're building greenfield then you want to try and be as non-commital as possible, if google raises their prices then you want to be able to jump ship to amazon, if amazon raises their prices, then jump ship to azure, if again you don't mind Alibaba jump ship there. There we have it that open source software has made at least early stage vendor lock in substantially less intense, you may have to change a front end piece of your code to change from Lambda Cloud to an IBM function, but you can still change. And if you're using containerized applications like docker, then you can change without really adjusting anything other than your deploy instructions. 

## More to be added...