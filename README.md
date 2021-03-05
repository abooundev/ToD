# ToD: Task-Oriented Dialogue

* 개념 자료

  * Deep Learning for Conversational AI  (Yun-Nung (Vivian) Chen [[page](https://sites.google.com/view/deepdial/)]

    * KAIST 2019 [[slides](https://www.google.com/url?q=https%3A%2F%2Fwww.csie.ntu.edu.tw%2F~yvchen%2Fdoc%2FKAIST19_Tutorial.pdf&sa=D&sntz=1&usg=AFQjCNE-mhpNtD_oMI5UZymRo5rX41_9Hw)] 

  * Princeton COS 598C (Spring 2020): Deep Learning for Natural Language Processing [[page](https://www.cs.princeton.edu/courses/archive/spring20/cos598C/lec16-task-oriented-dialogue)] 

    * lec16-task-oriented-dialogue [[silde](https://www.cs.princeton.edu/courses/archive/spring20/cos598C/lectures/lec16-task-oriented-dialogue.pdf)]

  * 대화 인터페이스, 챗봇, 그리고 자연어처리(서정연 교수) [[slide](https://sigai.or.kr/workshop/AI-for-everyone/2017/slides/대화-인터페이스-구현에-관련된-자연어-처리와-인공지능-기술-이야기.pdf)]

  * Stanford  Speech and Language Processing (3rd ed. draft) [[homepage](https://web.stanford.edu/~jurafsky/slp3/)]

    * CHAPTER 24 Dialog Systems and Chatbots [[note](https://web.stanford.edu/~jurafsky/slp3/24.pdf)], [[slide](https://web.stanford.edu/~jurafsky/slp3/slides/24_Dialogue_Jan_18_2021.pdf)]



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

- [ontology 구축 방법론 ](http://joyhong.tistory.com/attachment/cfile1.uf@125799354F9A03AE0F9007.pdf)


슬롯 태깅

현재 상태에서 필요한 정보를 엔티티 태깅을 통해 발화로부터 추출하는 프로세스

슬롯 필링(Slot Filling)

슬롯 태깅 결과, 유저 프로필 정보, 발화 히스토리(컨텍스트) 등을 전부 참조해서 최종 액션을 수행하기 위해 필요한 정보를 채워 넣는 과정

출처: https://tech.kakaoenterprise.com/58 [카카오엔터프라이즈 기술블로그 Tech&(테크앤)]



**슬롯**(slot)

발화에 포함된 태스크와 관련된 의미 있는 정보



All modern task-based dialogue systems, whether the simple GUS architecture dialogue state we describe here, or the more sophisticated dialogue state architectures we turn to frame in the following section, are based around frames. 

A **frame** is a kind of **knowledge structure representing the kinds of intentions** the system can extract from user sentences, and consists of **a collection of slots**, each of which can take a set of possible values. Together this **set of frames** is sometimes called **a domain ontology**



The **set of slots** in a task-based dialogue frame specifies what the system needs to know, and **the filler of each slot is constrained to values of a particular semantic type**. In the travel domain, for example, a slot might be of type city (hence take on values like San Francisco, or Hong Kong) or of type date, airline, or time.

 

Types in GUS, as in modern frame-based dialogue agents, have hierarchical structure; for example the date type in GUS is itself a frame with slots with types like integer or members of sets of weekday names: 

DATE 

MONTH:NAME YEAR:INTEGER DAY:(BOUNDED-INTEGER 1 31) WEEKDAY:(MEMBER (Sunday Monday Tuesday Wednesday Thursday Friday Saturday))

The goal of the natural language understanding component in the **frame-based architecture** is to extract <u>three things</u> from the user’s utterance. 

The first task is **domain classification**: is this user for example talking about airlines, programming an alarm clock, or dealing with their calendar? Of course this 1-of-n classification tasks is unnecessary for single-domain systems that are focused on, say, only calendar management, but multi-domain dialogue systems are the modern standard. 

The second is **user intent determination**: what general task or goal is the user trying to accomplish? For example the task could be to Find a Movie, or Show a Flight, or Remove a Calendar Appointment. Finally, we need to do **slot filling**: extract the particular **slots** and **fillers** that the user intends the system to understand from their utterance with respect to their intent. From a user utterance like this one:



24.4 The Dialogue-State Architecture 

Modern research systems for **task-based dialogue** are based on a more sophisticated version of the **frame-based architecture** called the **dialogue-state** or **belief-state architecture**. Figure 24.12 shows the **six components** of a typical dialogue-state system. The speech recognition and synthesis components deal with spoken language processing; we’ll return to them in Chapter 26. 

For the rest of this chapter we therefore consider the other **four components, which are part of both spoken and textual dialogue systems**. These four components are more complex than in the simple GUS systems. 

For example, like the GUS systems, the dialogue-state architecture has an **NLU component to extract slot fillers from the user’s utterance**, but generally using machine learning rather than rules. 

The **dialogue state tracker** maintains the **current state of the dialogue** (which include the user’s **most recent dialogue act**, plus the **entire set of slot-filler constraints** the user has expressed so far). 

The **dialogue policy** decides what the system should do or say next. The dialogue policy in GUS was simple: **ask questions until the frame was full and then report back the results of some database query.** But a more sophisticated dialogue policy can help a system **decide when to answer the user’s questions, when to instead ask the user a clarification question, when to make a suggestion, and so on.** 

Finally, dialogue state systems have a natural language generation component. In GUS, the sentences that the generator produced were all from pre-written templates. But a more sophisticated generation component can condition on the exact context to produce turns that seem much more natural. As of the time of this writing, most commercial system are architectural hybrids, based on GUS architecture augmented with some dialogue-state components, but there are a wide variety of dialogue-state systems being developed in research labs.





### Structure

<img src="https://image.slidesharecdn.com/170428hkust-170430013715/95/deep-learning-for-dialogue-systems-12-638.jpg?cb=1493516273">

출처: https://www2.slideshare.net/YunNungVivianChen/deep-learning-for-dialogue-systems

<img src="https://www.researchgate.net/profile/Trung_Bui/publication/302567766/figure/fig1/AS:360041279442952@1462851938643/Overview-of-the-dialog-state-tracking-system.png" alt="Overview of the dialog state tracking system.  " style="zoom: 80%;" />

출처: [Robust Dialog State Tracking for Large Ontologies](https://www.researchgate.net/publication/302567766_Robust_Dialog_State_Tracking_for_Large_Ontologies)


![image](https://user-images.githubusercontent.com/65707664/99775648-f99c1300-2b52-11eb-84bf-dddd18068d2a.png)

출처: [Kim, S., Yang, S., Kim, G., & Lee, S. W. (2019). Efficient dialogue state tracking by selectively overwriting memory. *arXiv preprint arXiv:1911.03906*.](https://arxiv.org/pdf/1911.03906.pdf)


### 참고
- What makes a good conversation? http://www.abigailsee.com/2019/08/13/what-makes-a-good-conversation.html
