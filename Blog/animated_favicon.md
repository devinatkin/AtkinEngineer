[Resume](../resume_page.md) [Projects](../projects.md), [Blog](../blog.md)

It's animated. It's a favicon... Need I say more. Well I probably should just cause I'm trying to be good about writing and keep people entertained with my words. 
- I made this using Claude: https://storage.googleapis.com/atkin_pages/bouncing-ball-favicon-site.html

It's not a perfect system and not everything will actually render animated favicons. And don't try and render anything too complicated as the bouncing ball indicates (It stutters). But there indeed some definite uses to having an animated favicon. The main one being loading, having a definite indicator that the website you're using is in fact working on things, even if it's running fairly slowly. This is actually the only use case I've seen; however, I'd honestly love to see more. If the little icon on the top animated a little smoother I'd be tempted to try rendering video in there, as it is there's lots of wasted potential there for taking advantage.

Big one being displaying a count. Think your google icon displaying an open envelope when you have mail, as opposed to the closed one. Or having an active count that updates when you get a new email. It's a small UI element but it would be handy to be able to see the count before clicking on the tab. I can imagine other counts being similarly improved through the addition of that small UI element. 

Identifying different tabs on the fly based on their contents. When you get to more than half a dozen tabs, you likely have a few copies of the same page open with different content, simply animating the favicon to adjust somewhat to the content would help tab collectors like myself. You're writing an email in one tab, and you're reading it in another. Have one tab show the standard email icon, have the other add a pen to it. 

This is certainly a beyond the good enough point but it's a nice touch that a few people would notice, and it'll naturally add a small improvement to their experience. At this time I'm adding a simple favicon to this site.

<script>
    const canvas = document.getElementById('faviconCanvas');
    const ctx = canvas.getContext('2d');
    const favicon = document.getElementById('favicon');

    function drawBall(angle) {
        // Clear the canvas
        ctx.clearRect(0, 0, 32, 32);

        // Save the current context state
        ctx.save();

        // Move the origin to the center of the canvas
        ctx.translate(16, 16);

        // Rotate the canvas context by the specified angle
        ctx.rotate(angle);

        // Draw the ball at the new origin
        ctx.beginPath();
        ctx.arc(0, 0, 8, 0, Math.PI * 2);
        ctx.fillStyle = '#007bff';
        ctx.fill();

        // Restore the original context state
        ctx.restore();
    }

    function updateFavicon() {
        const time = performance.now() / 1000;
        const angle = time * Math.PI; // Rotate at 1 radian per second
        drawBall(angle);
        favicon.href = canvas.toDataURL('image/png');
    }

    // Use setInterval for consistent updates, even when the tab is inactive
    setInterval(updateFavicon, 50);  // Update every 50ms (20 fps)

    // Optional: Use requestAnimationFrame for smoother animation when the tab is active
    function animateWhenVisible() {
        updateFavicon();
        requestAnimationFrame(animateWhenVisible);
    }
    requestAnimationFrame(animateWhenVisible);
</script>
