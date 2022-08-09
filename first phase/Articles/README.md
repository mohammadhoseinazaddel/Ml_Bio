

nastaran

**Deep Neural Networks Can Predict New Onset Atrial Fibrillation From the 12-Lead ECG and Help Identify Those at Risk of Atrial Fibrillation–Related Stroke**

<div dir="rtl">


-	پیش بینی با استفاده از ECG  12 کاناله  و سن
-	استفاده از متود deep learning
-	داده از 430 هزار بیمار در طول 35 سال گرفته شده و در مجمئع 1.6 میلیون داده از  Geisinger’s clinical   MUSE است
-	معیار مقایسه: roc curve, precisions-recall
-	62 درصد بیمارانی که پیش بینی شده بود دچار a-fib  بشوند در طول 3 سال به این بیماری دچار شدند
-	مقایسه گروه های normal و abnormal  به صورت جداگانه و مقایسه کلی با مدل Xgboost  که نتیجه بهتره گرفته 
 
</div>

**Artificial intelligence algorithm for predicting cardiac arrest using electrocardiography**
<div dir="rtl">

-	ب A-fib بی علایم یا دارای غلایم کمی است
-	47 هزار داده از 26 هزار بیمار در طول 3 سال
-	استفاده از روش learning-based artificial intelligence algorithm
-	پیش بینی با استفاده از ECG  12 کاناله  و سن و جنسیت
-	استفاده از 6 لید برای train  و 12 لید برای validation
-	دو لایه conv  و دو لایه batch normalization  یک لایه max pooling  و یک لایه drop out 
</div>

![image](https://github.com/mohammadhoseinazaddel/Ml_Bio/blob/main/statics/img/nas1.png)
<div dir="rtl">

-	معیار مقایسه بر اساس auroc
-	پیش بینی تا 24 ساعت قبل


**بایومارکرها**
 </div>
 
 ![image](https://github.com/mohammadhoseinazaddel/Ml_Bio/blob/main/statics/img/nas%20biomarkers.png)

mohammad hossein

***Machine predicts heart attacks 4 hours before doctors***

https://www.newscientist.com/article/mg22329814-400-machine-predicts-heart-attacks-4-hours-before-doctors/
<div dir="rtl">

پیش بینی زودهنکام قبل از اعلام کد آبی برای مریض با استفاده از داده های 133 هزار مریض که به NorthShore University HealthSystem که شامل 4 بیمارستان شیکاگو از سال2006 تا 2011 مراجعه کردند و 815 باز کد آبی برای آنها به صدا درآمدهو سیستمدر 2 سوم موارد درست پیش بینی کرده بود و  20 درصد false positive برای سکته قلبی داشته تیمPeter Donnan at the University of Dunde روش کار میکنه تا با دیتاهای بیمارستانای دیگه بهترش کنه و قرارهhttps://www.kdd.org/kdd2014/ ارایه بشه
 
 در مقاله 4 ام با استفاده از داده های مه در EMR که شامل ثبت تمامی اطلاعات حیاتی و آرمایشگاهی و عکس های بیماری و ناریخجه بیمار هست و با استقاده از روش هاس کلاسیک svm و Logestic بیمارا را به دو دسته که حال وخیم پیش میاد براشون و یا نه تقسیم بندی کردن و 30 درصد false positive داشتن
 
[EMR](https://en.wikipedia.org/wiki/Electronic_health_record)
 
 ![image](https://github.com/mohammadhoseinazaddel/Ml_Bio/blob/main/statics/img/art4%20hart%20rate%20temprature%20time%20series.png)
 
 ![image](https://github.com/mohammadhoseinazaddel/Ml_Bio/blob/main/statics/img/art4%20lab%20vital%20features.png)
 
 ![image](https://github.com/mohammadhoseinazaddel/Ml_Bio/blob/main/statics/img/art4%20fp.bmp)
 
</div>
Heart rate prediction model based on neural network

- This paper uses Long Short-Term Memory (LSTM) to avoid gradient explosions

- It considered five physiological characteristics included, heart rate signal, gender, age, physical activities and mental state.

- Network layers are:
1- 1 layer LSTM network model is added, which contains 50 neurons, with the activation function of tanh.
2- A fully connected Dense layer is added, with the activation function of linear.
3- Each layer is configured with the dropout rejection rate of 0.2 to prevent overfitting.
4- A fully connected layer is added, the activation function of ReLU to connect the hidden layer
and output.

- The number of samples batch size in each training is set as 128, with the training rounds epoch of 100.

- The data of this paper was collected by the laboratory, a total of 48 samples, with the sampling rate of 50Hz, and the data length ranging from 90s to 580s. The testee is a healthy young man without any history of heart disease, who maintains a good mental state and the physical activity is slow walking.

- When other parameters are the same, the effect of prediction by solely relying on the heart rate before the t moment is shown in this figure:

![image](https://user-images.githubusercontent.com/53640254/183687694-51401547-f456-42b5-aa32-0cded01451a0.png)

where Root Mean Square Error (RMSE) is 0.208

- In more complicated cases, such as the testee's more intense physical activities, more unstable mental state, and even the emergence of other diseases, the neural network prediction proposed in this paper has a great application prospect and potential.



**Real-Time System Prediction for Heart Rate Using Deep Learning and Stream Processing Platforms**

- Data Collection: Medical Information Mart for Intensive Care (MIMIC-II) is used and the heart rate time series from MIMIC-II dataset  on a minute-by-minute basis for one patient has been extracted.

- batch size: 1; learning rate: 0.0001; and epochs: 15

- The proposed real-time prediction system consists of two phases: the oﬄine phase and the online phase. In the oﬄine phase, RNN, LSTM, GRU, and BI-LSTM using one layer, two layers, and three hidden layers are used to train and evaluate HR time-series data.

- The best developed model for each case that has the lowest RMSE is used to evaluate the
system in real time.

- GRU model has recorded the best performance using three hidden layers.

![image](https://user-images.githubusercontent.com/53640254/183687951-ec3b4217-285f-4180-8a89-43e1e2814240.png)


- In the online phase, the developed simulation-based sensor generates HR time-series data and
sends them to the Kafka Topic. Then, Spark streaming reads HR data from the Kafka topic and sends them to the best developed model to predict HR in the near future 15 minutes in advance.

![image](https://user-images.githubusercontent.com/53640254/183688010-ff82abd4-c0f6-4c24-8cae-f0c450c75cea.png)


article 8 mohammad hossein

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8726033/

![](https://github.com/mohammadhoseinazaddel/Ml_Bio/blob/main/statics/img/only%205.png)

patent fatemeh

https://github.com/mohammadhoseinazaddel/Ml_Bio/edit/main/first%20phase/Articles/README.md

