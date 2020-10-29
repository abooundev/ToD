# ToD: Task-Oriented Dialogue

* 개념 자료

  * [대화 인터페이스, 챗봇, 그리고 자연어처리(서정연 교수)](https://sigai.or.kr/workshop/AI-for-everyone/2017/slides/대화-인터페이스-구현에-관련된-자연어-처리와-인공지능-기술-이야기.pdf)
  * https://www.cs.princeton.edu/courses/archive/spring20/cos598C/lectures/lec16-task-oriented-dialogue.pdf
  * https://www.slideshare.net/YunNungVivianChen/deep-learning-for-dialogue-systems

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
  * SOLOIST: https://arxiv.org/pdf/2005.05298.pdf

* Dataset

  * CrossWOZ: https://arxiv.org/pdf/2002.11893v2.pdf




### Dialogue subtasks

* dialogue understanding
* dialogue management
  * dialogue act classification
  * dialogue state tracking
  * task-completion dialogue policy learning
* dialogue generation

* slot filling




* Domain ontology: a set of knowledge structures representing the kinds of intentions the system can extract from user sentences. 
* Domain: a domain consists of a collection of slots. 
* Slot: each of slot can take a set of possible values.

도메인 온톨로지는 발화 문장에서 추출할 수 있는 의도에 대한 구조적인 표현이다.

The domain ontology defines the set of actions our model can take.

도메인 온톨로지는 모델이 취할 수 있는 행동들을 정의하고 있다.



https://sigport.org/sites/default/files/docs/MingHsiangSu-IALP%202016_3.pdf

https://web.stanford.edu/~jurafsky/slp3/24.pdf

https://sites.google.com/view/deepdial/

https://www.csie.ntu.edu.tw/~yvchen/doc/COLING18_Tutorial.pdf

https://speakerdeck.com/scatterlab/towards-universal-dialog-state-tracking?slide=7

