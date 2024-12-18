[Resume](../resume_page.md) [Projects](../projects.md), [Blog](../blog.md)

What AI Services am I using and why am I using those AI services.

## ChatGPT Premium and Open AI API
At time of writing this is the one ongoing premium account that I have. I am a fan of Open AI given they seem to have their act together in terms of actually rolling things out across the world as opposed to limiting themselves to a much smaller region. This makes it feel a lot fairer. That being said there are still certainly things I don't like, like waiting on their updates until they pass some ambiguous safety bar. Which sounds off given I quite like the fact that OpenAI is taking safety as seriously as they do. However, I think with things like say their Sora model, assuming they aren't cherry picking their results, they could setup their API with a mechanical turk stage of a real human validating the safety of the result. Yes this would be expensive, incredibly so, but at leasy they'd be releasing their model and letting more than a handful of people get familiar and play with it. I feel like a financial barrier to use is far more fair than an arbitrary we happen to have the right connection for you to be on our red teams to use the unsafe versions. 

### GPT-4o and GPT-4o mini
These models are solid incremental improvements, but nothing to really write home about. The cheapness of the mini model makes it a good candidate for long term AI applications, where the the full model can easily start to break the bank on applications which don't turn immediate significant profit. API wrapper companies that have based their entire product line on the Open AI hype-train are probably rolling in gravy given the fine tuning availability for the mini model, and the broad cheapness of it for piling out more generated content. 

## Amazon Bedrock (Amazon Tital Models & Everyone Elses)
Because I love having access to a Wide Selection of models I've been using Amazon bedrock whenever something new drops. From Claude Opus, to the variety of models from A21 and others it's been a great playground. Only thing I seriously wish is that amazon had a API setup for bedrock and AWS in general as it's annoying to get going with the automated calls. Amazon has a couple of cheap base models of their own, although I haven't heard much of people using them for more major applications. 

Probably my biggest critique of the platform is a central one with all AWS products. Splitting up the site by region and then product is honestly a terrible system. Regional avialability is of course always going to be a thing, as well as regional pricing thanks to different costs of doing business. But I don't want to have to guess which region I need to select to get the model I want. If I care about region (Which not everyone will, it's a narrowing selection that comes after the product). For instance, I can never remember where the latest and greatest Sonnet 3.5 is available, because I know it's available in one region, but not others. Then there's some regions like Canada with such a small selection of models that it seems a little silly, but i can see people caring about their data not crossing borders being grateful for the handful that are available.

If OpenAI and Google could shake hands and jump onto AWS for convenince sake it might be enough to keep me locked onto a singular site for all my AI needs. But as it is, I continue to explore because competitors will compete.

## Google AI Studio (Gemini Models)
Now this is one I've used for one feature and one feature alone. Video Processing. I honestly should build myself up a prettified little end point, but it's quite nice to be able to take one of my video files and then ask Gemini to create summaries or answer questions based on the videos. For longer videos, or ones that I want to post online  I've taken to asking it "Is there anything potentially revealing in this video (Names, Addressses, Logins, Etc)". When I make a video for an internal audience, but then it seems worth posting online this prompt can (With some risk of hallucination) act as a way to screen for accidental leaks. That being said I wouldn't trust it on its own. 

Honestly not sure why this page exists as opposed to being integrated into the existing Vertex AI section of the Google Cloud Platform, although it's not a bad setup regardless, just a bit confusing.

## LM Studio
Locally running LLMs. This works, mediocre at best. Perhaps it's just because the machines I run it on have all lacked large beefy GPUs to handle all the models. I mean I've had an Intel Arc but that's not going to be too great. That being said, for quickly playing around with models like Gemma it's very nice. For larger models, I really don't recommend interacting in real time as that just always sucks. Some of the models do have reasonably large input context windows and when those are actually full I've had it take upto 10 minutes to start producing output. So yeah, that was not a great time all things being equal. 

### Google Gemma 2B
With LM studio Google Gemma will run on most machines. It's not suitable for a lot of applications as the performance is relatively speaking quite poor; however, given it would run happily on a phone level of hardware, it's a good sign of what's to come. Many will dismiss the 8B and lower models as not worth the time; however, they can actually have some of the largest impact as they can be run without the normal bottlenecks of networking and lightspeed. 

| Metric               | Value    |
|----------------------|----------|
| Time to first token  | 2.42s    |
| Generation time      | 28.79s   |
| Speed                | 7.55 tok/s |
| Stop reason          | eosFound |
| GPU layers           | 0        |
| CPU threads          | 16       |
| Mlock                | true     |
| Token count          | 256/2048 |

This low is running with a system setup incredibly poorly for running these types of setups. And it's still able to achieve a usable 7.5 tokens per second. With a system contianing a basic gpu setup, or one of the newer processors containing a simple tpu I have no doubts this model would be properly snappy in performance. Rembering that with these tiny models it becomes exceptionally improtant to not overdo it with regards to knowledge base, even basic information should really be provided to prevent the system from going off the deepend when asked to perform even simple tasks. 

### Llama 3.1 8B
3.1 Dropped just the other day at time of writing with models ranging in size from a GPT-4o competitor at well over 405B parameters and several hundred gigabytes of weights, to the tiny 8B parameter model. The relative openness of this model is really what makes it win in the eyes of most people. I may not have a massive bank of GPUs to run the large model, but there's nothing stopping me from spinning them up and giving it a go. Just expect a truely eye watering AWS bill at the end of the month. 

| Metric               | Value    |
|----------------------|----------|
| Time to first token  | 3.83s    |
| Generation time      | 40.10s   |
| Speed                | 5.27 tok/s |
| Stop reason          | eosFound |
| GPU layers           | 0        |
| CPU threads          | 16       |
| Mlock                | true     |
| Token count          | 262/2048 |

With the similarly terrible hardware for the application the 8B token model performs surprisingly well. The drop in tokens per second is expected given the model is 4 times larger. I could likely get an impressive improvement moving from my GPU-less setup to even a basic model where some of the operations can be offloaded to the GPU. 

## Claude ... 
Well this is why you release globally as quickly as possible. I had thought that it might have pulled me away from Open AI. But I'm used to Open AI's responses. And as cool as their artifacts are, they aren't cool enough to have me pull my subscription from ChatGPT and seriously make a switch over. It's not a particularly advanced feature and I'm sure it's only a matter of time before ChatGPT has something similar. Or given their tie in with microsoft why not make those artifacts, on github. Or allow it to make basic pull requests to start branches. These features will eventually hit parity and it'll just be a matter as to who has the better model combined with whose user interface best makes the model useful in the individuals workflow. 

Claude could have been the winner there if they'd been available sooner in my Area. The other day I decided to give Claude a generous try and get it to prep a simple webpage with an animated favicon. It didn't do it correctly immediately; however, their artifact setup was definitely cleaner and more user friendly than any of the other setups which I've seen producing a rapid functional, if nowhere near perfect result [Claude Page](https://storage.googleapis.com/atkin_pages/bouncing-ball-favicon-site.html). I feel like for small businesses setting up simple webpages to represent their business they'd be in exactly the right place. Throw together a site using Claude and then host the HTML on a basic data bucket to simply tell people who and what you are. 

## Sora
Mmmm... I love AI generated slop in the mornings. Sora was released recently with the Open AI shipmas. And I've gotta say the downgrades between the very specifically picked for quality ouptuts given by Sora in the demo videos versus the quality given by random prompts given by users is quite a startling drop. Although thier showcase page won't make it seem that terrible. 

From animation that looks like its being done with microsoft paint, to horrifying eldrige horrors with way more eyes than they're supported to have. Sora will ocassionally produce charming outputs. But it will also make you want to run away screaming. Is Sora the death of low end stock video. Yes, paying $200 a month for the pro account so you can generate unlimited videos and then sorting through for the gems that actually meet your requirements is a very valid approach that's going to be cheaper and more specific than a traditional lets go buy the real video from some poor shlup who'll make a small amount off of the agreement so you can use it in your demo video. If the model continues to improve at the same rate that models like Dalle have, then in a few years it'll be good enough for 90% of stock video. 