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

