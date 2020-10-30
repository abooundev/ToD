# ToD: Task-Oriented Dialogue

* 개념 자료

  * Deep Learning for Conversational AI  (Yun-Nung (Vivian) Chen [[page](https://sites.google.com/view/deepdial/)]

    * KAIST 2019 [[slides](https://www.google.com/url?q=https%3A%2F%2Fwww.csie.ntu.edu.tw%2F~yvchen%2Fdoc%2FKAIST19_Tutorial.pdf&sa=D&sntz=1&usg=AFQjCNE-mhpNtD_oMI5UZymRo5rX41_9Hw)] 

  * Princeton COS 598C (Spring 2020): Deep Learning for Natural Language Processing [[page](https://www.cs.princeton.edu/courses/archive/spring20/cos598C/lec16-task-oriented-dialogue)] 

    * lec16-task-oriented-dialogue [[silde](https://www.cs.princeton.edu/courses/archive/spring20/cos598C/lectures/lec16-task-oriented-dialogue.pdf)]

  * 대화 인터페이스, 챗봇, 그리고 자연어처리(서정연 교수) [[slide](https://sigai.or.kr/workshop/AI-for-everyone/2017/slides/대화-인터페이스-구현에-관련된-자연어-처리와-인공지능-기술-이야기.pdf)]

  * Stanford  Speech and Language Processing (3rd ed. draft) [[homepage](https://web.stanford.edu/~jurafsky/slp3/)]

    * CHAPTER 24 Dialog Systems and Chatbots [[note](https://web.stanford.edu/~jurafsky/slp3/24.pdf)]

      

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








