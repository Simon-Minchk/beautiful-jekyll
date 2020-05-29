<html>
<body>
<p style="font-size:50px;color:red;">WARNING</p>
</body>
</html>

Before going into what I found using this dataset I would like to say that you shouldnt use this knowledge without doing more research, I have little to no knowledge on mushrooms and for all I know, the information in the dataset could be wrong or inaccurate. All I am doing in this blog post is exploring this dataset making connections and predictions for fun. 

This dataset I used was all about mushrooms and had a ton of features to use in a model and a nice simple target class to predict, is it edible or poisonous. I started out by finding a baseline, for that I just predicted the most common result which was that it was edible, this would give an accuracy of about 52%. Next, I started looking through how all the features compared to the target class. I found right away that the most telling signs that a mushroom is edible or not were more distinct features like color, odor, and whether or not it bruise. I set up my model, split the data into my train, val, test sets and wrangled everything together dropping a few features that had almost random results. When I did my first model test it came back as 100% which made me worried that I had data leakage but as I found out from more exploring its literally just that accurate. After removing all but a select few features I managed to get the test score to just under 100% so that it wouldnt look as questionable. A fun thing I found while selecting features was that odor, by itself was able to reach 98% accuracy which is insanely accurate for a single feature. The image below shows how  odor correlates with edibility and as you can see each smell usually is either completely edible or completely poisonous with the only exception being no smell.
![Crepe](https://i.gyazo.com/96614313865713a18f5cd781dd99fed0.png)
<br>
Here I have another image showing a crosstab between them, its pretty clear to see why the model was able to reach 98% with odor alone.
![Crepe](https://i.gyazo.com/413812b68cfe5c2485a01e0aa26c9168.png)
<br>

![Crepe](https://i.gyazo.com/95f881605c3a9b9527d6c4d02e72aba2.png)
<br>

![Crepe](https://i.gyazo.com/e7f8ca97facac4363c7b7c4491046445.png)
<br>

You can find my notebook <a href="https://colab.research.google.com/drive/1kf_AvXFXsRE280SIYOV19M0v2RYLARe9?usp=sharing">HERE</a>    
You can find the data set <a href="https://www.kaggle.com/uciml/mushroom-classification">HERE</a>
