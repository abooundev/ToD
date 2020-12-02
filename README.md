# ToD: Task-Oriented Dialogue

* 개념 자료

  * Deep Learning for Conversational AI  (Yun-Nung (Vivian) Chen [[page](https://sites.google.com/view/deepdial/)]

    * KAIST 2019 [[slides](https://www.google.com/url?q=https%3A%2F%2Fwww.csie.ntu.edu.tw%2F~yvchen%2Fdoc%2FKAIST19_Tutorial.pdf&sa=D&sntz=1&usg=AFQjCNE-mhpNtD_oMI5UZymRo5rX41_9Hw)] 

  * Princeton COS 598C (Spring 2020): Deep Learning for Natural Language Processing [[page](https://www.cs.princeton.edu/courses/archive/spring20/cos598C/lec16-task-oriented-dialogue)] 

    * lec16-task-oriented-dialogue [[silde](https://www.cs.princeton.edu/courses/archive/spring20/cos598C/lectures/lec16-task-oriented-dialogue.pdf)]

  * 대화 인터페이스, 챗봇, 그리고 자연어처리(서정연 교수) [[slide](https://sigai.or.kr/workshop/AI-for-everyone/2017/slides/대화-인터페이스-구현에-관련된-자연어-처리와-인공지능-기술-이야기.pdf)]

  * Stanford  Speech and Language Processing (3rd ed. draft) [[homepage](https://web.stanford.edu/~jurafsky/slp3/)]

    * CHAPTER 24 Dialog Systems and Chatbots [[note](https://web.stanford.edu/~jurafsky/slp3/24.pdf)]

  * Natural Language Processing 

    * State tracking in DM [[lecture](https://www.coursera.org/lecture/language-processing/state-tracking-in-dm-s9zRt)]
  
  * [우리말 자연어 처리 기술](https://www.korean.go.kr/nkview/nklife/2017_4/27_0404.pdf)
    

* Survey

  * Recent Advances and Challenges in Task-oriented Dialog Systems: https://arxiv.org/pdf/2003.07490.pdf

  * Neural Approaches to Conversational AI: https://arxiv.org/pdf/1809.08267.pdf

  * 심층 신경망 기반 대화처리 기술 동향: https://ettrends.etri.re.kr/ettrends/178/0905178006/34-4_55-64.pdf

  * 목적지향 대화 시스템을 위한 챗봇 연구: https://scienceon.kisti.re.kr/srch/selectPORSrchArticle.do?cn=JAKO201734963782120&dbt=NART

    

* Paperwithcode

  * Task-Oriented Dialogue Systems: https://paperswithcode.com/task/task-oriented-dialogue-systems

  

* 모델

  * ToD-BERT
    * https://github.com/modulabs/beyondBERT/issues/17
  * SimpleToD
    * [blog](https://blog.einstein.ai/simpletod/)
    * https://github.com/modulabs/beyondBERT/issues/18 
  * SOLOIST
    * https://arxiv.org/pdf/2005.05298.pdf

* **Dialog State Tracking**

  * Towards Universal **Dialog State Tracking**
    * https://speakerdeck.com/scatterlab/towards-universal-dialog-state-tracking?slide=7
  * **Dialog State Tracking** and **Action Selection** Using Deep Learning Mechanism for Interview Coaching
    * [https://sigport.org/sites/default/files/docs/MingHsiangSu-IALP%202016_3.pdf](https://sigport.org/sites/default/files/docs/MingHsiangSu-IALP 2016_3.pdf)

* Dataset

  * CrossWOZ
    * https://arxiv.org/pdf/2002.11893v2.pdf




### Dialogue subtasks

* dialogue understanding
* dialogue management
  * dialogue act classification
  * dialogue state tracking
  * task-completion dialogue policy learning
* dialogue generation

* slot filling



### Memo


* Domain ontology: a set of knowledge structures representing the kinds of intentions the system can extract from user sentences. 
* Domain: a domain consists of a collection of slots. 
* Slot: each of slot can take a set of possible values.

The domain ontology defines the set of actions our model can take.



### Structure

<img src="https://image.slidesharecdn.com/170428hkust-170430013715/95/deep-learning-for-dialogue-systems-12-638.jpg?cb=1493516273">

출처: https://www2.slideshare.net/YunNungVivianChen/deep-learning-for-dialogue-systems

<img src="https://www.researchgate.net/profile/Trung_Bui/publication/302567766/figure/fig1/AS:360041279442952@1462851938643/Overview-of-the-dialog-state-tracking-system.png" alt="Overview of the dialog state tracking system.  " style="zoom: 80%;" />

출처: [Robust Dialog State Tracking for Large Ontologies](https://www.researchgate.net/publication/302567766_Robust_Dialog_State_Tracking_for_Large_Ontologies)


![image](https://user-images.githubusercontent.com/65707664/99775648-f99c1300-2b52-11eb-84bf-dddd18068d2a.png)

출처: [Kim, S., Yang, S., Kim, G., & Lee, S. W. (2019). Efficient dialogue state tracking by selectively overwriting memory. *arXiv preprint arXiv:1911.03906*.](https://arxiv.org/pdf/1911.03906.pdf)

