<html>
<body>
<p style="font-size:50px;color:red;">WARNING</p>
</body>
</html>

Before going into what I found using this dataset I would like to say that you shouldnt use this knowledge without doing more research, I have little to no knowledge on mushrooms and for all I know, the information in the dataset could be wrong or inaccurate. All I am doing in this blog post is exploring this dataset making connections and predictions for fun. 


This dataset I used was all about mushrooms. There were a ton of features to use and a nice simple target class to predict, is it edible or poisonous. I started out by finding a baseline, for that I just predicted the most common result which was that it was edible. This gave me an accuracy of about 52%. Next, I started looking through how all of the features compared to the target class. I found right away that the most telling signs that a mushroom is edible or not were more distinct features like color, odor, and whether or not it bruised. I set up my model, split the data into my train, validation, and test sets and wrangled everything together dropping a few features that had almost random results. When I did my first model test it came back as 100% which made me worried that I had data leakage but as I found out from more exploring its literally just that accurate. After removing all but a select few features I managed to get the test score to just under 100% so that it wouldnt look as questionable. A fun thing I found while selecting features was that odor, by itself was able to reach 98% accuracy which is insanely accurate for a single feature. The image below shows how odor correlates with edibility and as you can clearly see each smell usually is either completely edible or completely poisonous with the only exception being no smell at all.

![Crepe](https://i.gyazo.com/96614313865713a18f5cd781dd99fed0.png)
<br>

Here I have another image showing a crosstab between them, its pretty clear to see why the model was able to reach 98% with odor alone.

![Crepe](https://i.gyazo.com/413812b68cfe5c2485a01e0aa26c9168.png)
<br>

With my predictive model being such a great success I wanted to try to find out which features really were the most important find out if I could use any of of this in real life. I'm no mushroom expert and I have no idea how to apply most of these features in real life so I tried to only use ones that were easily understood. The below image is comparing the color of the mushrooms stalk below the ring to edibility, note that the color of the stalk above the ring had an almost identical graph so I didnt include it for that reason.

![Crepe](https://i.gyazo.com/95f881605c3a9b9527d6c4d02e72aba2.png)
<br>

As you can see from the graph, there are a few colors that we wouldnt want to take chances on, like white and pink. But it does still give us good information like what we can almost know for sure is bad or good. Brown, Buff, and Cinnamon are usually always poisonous and Grey, Orange, and Red are almost always edible.

The next most reliable feature to use in real life is whether or not it bruises. This one made me do a bit of research to understand how it worked but I believe I can explain it well enough now. Basically, if you nick a few parts of the mushroom and it starts to show any color change, it bruises. For the most part, If it bruises its much more likely to be edible (81%), and if it doesnt bruise its more likely to be poisonous although thats only 69% of the time. The graph below shows it nicely.

![Crepe](https://i.gyazo.com/e7f8ca97facac4363c7b7c4491046445.png)
<br>

Overall this dataset gave me a good exploration into the edibility of mushrooms and was fun to work with. However I would once again like to say that you should never use any of this knowledge without doing more research first, this dataset was originally made over 30 years ago and its possibly outdated or filled with wrong infomation. Please find and use an actual survival guide if you plan on ever being in the wild and or in a situation where you need to know which types of mushrooms are edible.

Thanks for reading!

You can find my notebook <a href="https://colab.research.google.com/drive/1kf_AvXFXsRE280SIYOV19M0v2RYLARe9?usp=sharing">HERE</a>    
You can find the data set <a href="https://www.kaggle.com/uciml/mushroom-classification">HERE</a>
