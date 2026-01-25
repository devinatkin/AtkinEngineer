[Work With Me](../resume_page.md), [Projects](../projects.md), [Blog](../blog.md)

It's animated. It's a favicon... Need I say more. Well I probably should just cause I'm trying to be good about writing and keep people entertained with my words. 
- I made this using [Claude Artifacts](https://storage.googleapis.com/atkin_pages/bouncing-ball-favicon-site.html)

It's not a perfect system and not everything will actually render animated favicons. And don't try and render anything too complicated as the bouncing ball indicates (It stutters). But there indeed some definite uses to having an animated favicon. The main one being loading, having a definite indicator that the website you're using is in fact working on things, even if it's running fairly slowly. This is actually the only use case I've seen; however, I'd honestly love to see more. If the little icon on the top animated a little smoother I'd be tempted to try rendering video in there, as it is there's lots of wasted potential there for taking advantage.

Big one being displaying a count. Think your google icon displaying an open envelope when you have mail, as opposed to the closed one. Or having an active count that updates when you get a new email. It's a small UI element but it would be handy to be able to see the count before clicking on the tab. I can imagine other counts being similarly improved through the addition of that small UI element. 

Identifying different tabs on the fly based on their contents. When you get to more than half a dozen tabs, you likely have a few copies of the same page open with different content, simply animating the favicon to adjust somewhat to the content would help tab collectors like myself. You're writing an email in one tab, and you're reading it in another. Have one tab show the standard email icon, have the other add a pen to it. 

This is certainly a beyond the good enough point but it's a nice touch that a few people would notice, and it'll naturally add a small improvement to their experience. At this time I'm adding a simple favicon to this site.

<link id="favicon" rel="icon" href="/favicon.ico">
<script>
document.addEventListener('DOMContentLoaded', function() {
    const faviconLink = document.getElementById('favicon') || document.querySelector("link[rel~='icon']");
    if (!faviconLink) {
        console.error('Favicon link element not found');
        return;
    }

    const canvas = document.createElement('canvas');
    canvas.width = 32;
    canvas.height = 32;
    const ctx = canvas.getContext('2d');
    const img = new Image();

    img.onload = function() {
        function updateFavicon() {
            const time = performance.now() / 1000;
            const angle = time * Math.PI / 4; // Rotate 45 degrees per second

            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.save();
            ctx.translate(canvas.width / 2, canvas.height / 2);
            ctx.rotate(angle);
            ctx.drawImage(img, -img.width / 2, -img.height / 2);
            ctx.restore();

            faviconLink.href = canvas.toDataURL('image/png');
        }

        // Start the animation loop
        function animateWhenVisible() {
            updateFavicon();
            requestAnimationFrame(animateWhenVisible);
        }
        requestAnimationFrame(animateWhenVisible);
    };

    img.src = faviconLink.href; // Load the existing favicon
});
</script>
