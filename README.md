# ShotPlot Computer Vision Archery App

[Try out ShotPlot on Heroku!](https://lw-shotplot.herokuapp.com)

I've long been fascinated by computer vision and had been thinking about using it to develop an automatic archery scoring system for a while. A few years ago, I found out about an archery range (shout out to [Gotham Archery](https://www.got-archery.com/)!) that had just opened in my neighborhood and decided to check it out. I was hooked after the introductory class and have been shooting there regularly ever since. As I continued to work on improving my form, I found self-evaluation to be somewhat difficult and wanted to come up with a quick and simple way to calculate my scores and shot distributions. As I developed my skills at the Metis data science bootcamp, I started to get a clearer vision of how exactly I could build such a tool. My initial app idea involved live object tracking running on a mobile device, which I quickly realized might be too ambitious for a computer vision neophyte. I eventually settled on a plan to analyze a single target photo to derive shot positions and an average shot score for the session.

### Data Collection

Before gathering my initial data, I set some restrictions on what each of those images would require. I wanted images to have all four corners of the target sheet visible so I could unskew and uniformly frame each one. Photos also needed to have enough contrast to pick out the target sheet and shot holes from the background. In order to keep the scope of the project manageable, I only used a single type of target: the traditional single-spot, ten ring variety. With those parameters in mind, I collected target data in two ways over several trips to the aforementioned [Gotham Archery](https://www.got-archery.com/); I used my iPhone to photograph my target after each round of shooting at the range and also collected several used targets others had shot from the range's discard bin. I set up a small home studio to quickly shoot the gathered targets but did not use any special lighting, camera equipment, or a tripod because I wanted the images to represent what an app user could easily produce themselves. I ended up collecting around 40 usable targets (some were too creased or torn) and set aside eleven of those to use as a test set to evaluate the app's performance.

![Images of used targets shot in different locations](img/targets.jpg)