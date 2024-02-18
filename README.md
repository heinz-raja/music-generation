# music-generation
Using GANs and LSTMs to create artificial music

This model generates new music by training on original compositions.

The initial approach was to convert songs to a series of images as shown below

![image](https://github.com/heinz-raja/music-generation/assets/41283762/15d70391-03b1-4c73-a8c0-21e561ff1ab0)

Then these images would be used to train the GAN. The results were not very impressive which is expected as GANs need a huge amount of data moreover since a song is multiple images, the context between images is lost and thus the new images produced would not be coherant. You can listen to one of the samples below 


https://github.com/heinz-raja/music-generation/assets/41283762/ec8c5498-80f4-4284-937e-a322143307cf

There are a lot of random pauses and offkey notes I also observed mode collapse and non convergence. 

For the next approach I used LSTMs and worked with the audio directly. LSTMs are good because they make use of sequential information and can recognize long term patterns. This provided much better results and actually made use of chords and notes which are in key. You can listen to a sample below. 


https://github.com/heinz-raja/music-generation/assets/41283762/8822637d-e3be-42fc-a48a-fa867b6d80b1

Results are much better however this just plays the next set of notes which fit in, there is work to be done in creating a 'story' with different sections with buildup and resolution.

