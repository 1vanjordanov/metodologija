# Одговори на прашања
# Прашање 1: Цитирање на труд со IEEE стил 

Како труд за својот колквиум сакав да изберам труд од MRI областа бидејќи од предавањата ми се видоа преинтересни визуелизациите и навистина сакав во краткиот период да се обидам да истражам нешто околку тоа. (Извинете однапред доколку некои термини не ги преведувам точно)

Трудот кој го избрав е *[Rapid T1 quantification from high resolution 3D data with model‐based reconstruction](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.27502?fbclid=IwAR2wjkoAv3OmFYvUFc3tpKg9p8MRdqK6LcwkyVgrKrs21-ynG2zAigHXWto)* од прв автор Oliver Maier, последен автор Rudolf Stollberger.

Бидејќи прв пат цитирам труд до сега, успеав да го најдам следниот линк кој од обично doi на труд генерира citation со IEEE стил.  ([линк до генератор](https://www.citationmachine.net/bibliographies/7f3b2e7e-3b28-4157-9984-263aaa49c8fd)<br> 


<i> O. Maier, J. Schoormans, M. Schloegl, G. J. Strijkers, A. Lesch, T. Benkert, T. Block, B. F. Coolen, K. Bredies, and R. Stollberger, “Rapid T 1 quantification from high resolution 3D data with model‐based reconstruction,” Magnetic Resonance in Medicine, vol. 81, no. 3, pp. 2072–2089, 2018.</i>



# Прашање 2: Опис на методологија на трудот 
## a) Квалитативно / Квантитативно

**Квантитативно истражување**


<img src="https://onlinelibrary.wiley.com/cms/asset/d8d8a6ad-7054-41af-9478-61f1fc562ad1/mrm27502-fig-0006-m.png" align='right' height="260"> 


**Образложение**: Крајната цел на трудот е да ја истражи врската помеѓу две квантитативни вредности кои се покажни во Фигура 5, и да покаже декадека времето потребно за собирање на податоците со овој предложен метод е побрзо и притоа го задржува квалитетот. Од самиот опис на фигурата 5 авторите  употребуваат 2D histogram contour plot каде се прикажуваат Т1 вредности без и со користење на VFA методот. Самите color мапи енкодираат области кои се заеднички voxel вредности и се трансформираат користејќи експоненцијално скалирање. Црвената линија индицира 45 степени, што кореспондира на совршено преклопување. 

Се користи [Pearson Correlation coefficient](http://learntech.uwe.ac.uk/da/default.aspx?pageid=1442) за да се прикаже зависноста помеѓу различно добиените вредности на истите податоци. 



## б) Собирање податоци 
Преформансот на предложениот модел се испитува врз предложен framework анализиран за Т1 quantification од 3D golden‐angle radial [VIBE (RAVE)](https://scholar.google.com/scholar_lookup?hl=en&volume=5&publication_year=2013&pages=6-11&journal=MAGNETOM+Flash&author=KT+Block&author=H+Chandarana&author=G+Fatterpekar&title=Improving+the+robustness+of+clinical+T1%E2%80%90weighted+MRI+using+radial+VIBE) податоци. 

## в) Хипотеза 
Хипотезата во трудот не е јасно дефинирана, но во "Purpose" секцијата е наведена целта: Трудот има цел да предложи модел кој би ги намалил времето на собирање на квантитативните  информации, бидејќи голем број не мерења во параметриски домен се испитуваат. 

(Од трудот: "To facilitate the clinical applicability, accelerating the acquisition is of high importance. To this end, we propose a model‐based optimization framework in conjunction with undersampling 3D radial stack‐of‐stars data.")

## г) Статистички тест 
Нема јасно дефиниран статистички тест со кој би се потрврдила/одбила хипотезата, но за утврдување на разликите/грешките на резултатите од податоци кои не го користат предложениот модел и оние кои го користат се употребуваат MRAE и corresponding error maps. 

(Од трудот: "Figure 1 shows the comparison of simulated MRI phantom reconstructions from undersampled VFA data to the numerical T1 reference. Visually, no difference is observable between 2D and 3D, respectively joint and separate regularization. TV and TGV regularized results show lower noise levels than L1‐wavelet results. The difference between the regularization strategies becomes evident by looking at corresponding error maps in Figure 2 and the mean relative absolute error (MRAE) respecively structural similarity index (SSIM) of the whole volume.") 

## д) Видови визуелизација
Се користат **хистограми** (за да се прикажат мапите од мозокот) како и **2D histogram contour plot** кои ја покажуваат зависноста на различно добиените вредности (модели кои користат VFA и кои не користат) на истите податоци. Во прилижениот пример од авторите се употребува програмскиот јазик Python и библиотеката <code>matplotlib</code>. 

## ѓ) Потврдување / одбивање на хипотеза 
Според заклучокот на трудот предложениот метод го редуцира времето потребно за собирање на податоците за 1.8-1.1 s/slice за VFA, со што технички "хипотезата" се **потврдува**, и целта на трудот е исполнета. 

(Од трудот: "With the proposed method it was possible to reconstruct 1 mm3 isotropic T1 maps from highly undersampled radially acquired data. Acquisition time could be reduced to 1.8–1.1 s/slice for VFA and 8 s/slice for IRLL data while preserving excellent quantitative accuracy. Reconstructions showed a gain in image fidelity compared to the fully sampled reference even for moderate to high acceleration. This was achieved by utilizing 3D TGV2 regularization combined with a spectral Frobenius norm to maximize the acceleration potential. We have further shown that the proposed solution strategy is applicable to different types of model‐based quantification problems.")



