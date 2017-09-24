sjCHAPTER 2

# Python Refresher

In the previous chapter, we took a journey into the world of natural language and exploredseveral interesting concepts and areas associated with it. We now have a better understandingof the entire scope surrounding natural language processing (NLP), linguistics, and textanalytics. If you refresh your memory, we had also got our first taste of running Python code toaccess and use text corpora resources with the help of the NLTK platform.

In this chapter, we will cover a lot of ground with regard to the core components andfunctionality of Python as well as some of the important libraries and frameworks associatedwith NLP and text analytics. This chapter is aimed to be a refresher for Python and forproviding the initial building blocks essential to get started with text analytics. This bookassumes you have some knowledge of Python or any other programming language. If you area Python practitioner, you can skim through the chapter, since the content here starts withsetting up your Python development environment and moves on to the basics of Python.

Our main focus in the chapter will be exploring how text data is handled in Python,including data types and functions associated with it. However, we will also be coveringseveral advanced concepts in Python, including list comprehensions, generators, anddecorators, which make your life easier in developing and writing quality and reusablecode. This chapter follows a more hands-on approach than the previous chapter, and wewill cover various concepts with practical examples.

```
이전 장에서 우리는 자연 언어의 세계로 들어가고 흥미로운 개념과 관련된 여러 영역을 탐구했습니다. 이제 자연 언어 처리 (NLP), 언어학 및 텍스트 분석을 둘러싼 전체 범위를 더 잘 이해하게되었습니다. 메모리를 새로 고침하면 Python 코드를 실행하여 NLTK 플랫폼을 사용하여 텍스트 코퍼 리소스를 사용하는 첫 번째 맛을 느낄 수있었습니다.

이 장에서는 파이썬의 핵심 구성 요소 및 기능뿐만 아니라 NLP 및 텍스트 분석과 관련된 중요한 라이브러리 및 프레임 워크와 관련하여 많은 부분을 다룰 것입니다. 이 장은 Python을 다시 생각하고 텍스트 분석을 시작하는 데 필요한 기본 구성 요소를 제공하기위한 것입니다. 이 책은 파이썬이나 다른 프로그래밍 언어에 대한 지식이 있다고 가정합니다. 파이썬 실무자라면이 장을 보지 않아도됩니다. 여기서 내용은 파이썬 개발 환경을 시작하고 파이썬의 기초로 넘어 가기 시작합니다.

이 장의 주요 초점은 텍스트 데이터가 파이썬에서 처리되는 방법과 관련된 데이터 유형 및 함수를 탐색하는 것입니다. 그러나 목록 작성, 생성자 및 데코레이터를 포함하여 Python의 여러 가지 고급 개념을 다루므로 품질 및 재사용 가능 코드 개발 및 작성 작업이 쉬워집니다. 이 장은 이전 장보다 실제적인 접근법을 따르며 실용적인 예제로 다양한 개념을 다룹니다.
```



## Getting to Know Python

Before we can dive into the Python ecosystem and look at the various components
associated with it, we must look back at the origins and philosophy behind Python
and see how it has evolved over time to be the choice of language powering many
applications, servers, and systems today. Python is a high-level open source general-
purpose programming language widely used as a scripting and across different domains.
The brainchild of Guido Van Rossum, Python was conceived in the late 1980s as a
successor to the ABC language, and both were developed at the Centrum Wiskunde and
Informatica (CWI), Netherlands. Python was originally designed to be a scripting and
interpreted language, and to this day it is still one of the most popular scripting languages
out there. But with object-oriented programming (OOP) and constructs, you can use

it just like any other object-oriented language, such as Java. The name Python, coinedby Guido for the language, does not refer to the snake but the hit comedy show MontyPython’s Flying Circus, since he was a big fan.

```
파이썬 생태계에 대해 살펴보고 파이썬과 관련된 다양한 구성 요소를 살펴보기 전에 파이썬의 근원과 철학을 되돌아 봐야합니다.
오늘날 많은 응용 프로그램, 서버 및 시스템에 전력을 공급하는 언어의 선택으로 시간이 지남에 따라 어떻게 발전해 왔는지보십시오. 파이썬은 스크립팅 및 다른 영역에서 널리 사용되는 고급 오픈 소스 범용 프로그래밍 언어입니다. 귀도 반 로섬 (Guido Van Rossum)의 개척자 인 파이썬은 1980 년대 후반 ABC 언어의 후계자로 잉태되었으며, 둘 다 네덜란드의 Centrum Wiskunde와 Informatica (CWI)에서 개발되었습니다. 파이썬은 원래 스크립팅 및 해석 언어로 설계되었으며 현재까지도 여전히 가장 인기있는 스크립팅 언어 중 하나입니다. 그러나 객체 지향 프로그래밍 (OOP) 및 구문을 사용하면 Java와 같은 다른 객체 지향 언어와 같습니다. Guido가 언어로 만든 파이썬이라는 이름은 뱀이 아니라 히트 코미디 쇼인 Monty Python의 Flying Circus를 가리킨다. 그가 팬 이었기 때문에.
```

As mentioned, Python is a general-purpose programming language that supportsmultiple programming paradigms, including the following popular programmingparadigms:

• Object-oriented programming
• Functional programming
• Procedural programming
• Aspect-oriented programming

```
앞서 언급했듯이, Python은 다음과 같은 보편적 프로그래밍 패러다임을 비롯한 여러 프로그래밍 패러다임을 지원하는 범용 프로그래밍 언어입니다.

• 객체 지향 프로그래밍
• 기능적 프로그래밍
• 절차적 프로그래밍
• Aspect 지향 프로그래밍
```



A lot of OOP concepts are present in Python, including classes, objects, data, andmethods. Principles like abstraction, encapsulation, inheritance, and polymorphism canalso be implemented and exhibited using Python. There are several advanced featuresin Python, including iterators, generators, list comprehensions, lambda expressions, andseveral modules like itertools and functools, which provide the ability to write codefollowing the functional programming paradigm.

```
클래스, 객체, 데이터, 메소드를 포함한 많은 OOP 개념이 파이썬에 존재합니다. 추상화, 캡슐화, 상속 및 다형성과 같은 원칙은 Python을 사용하여 구현되고 전시 될 수 있습니다. iterators, generator, list comprehensions, lambda expressions, itertools, functools와 같은 Python의 몇 가지 고급 기능이 있습니다.이 모듈은 함수 프로그래밍 패러다임에 따라 코드를 작성할 수있는 기능을 제공합니다.
```

Python was designed keeping in mind the fact that simple and beautiful code is
more elegant and easy to use rather than doing premature optimization and writing
hard-to-interpret code. Python’s standard libraries are power-packed with a wide variety
of capabilities and features ranging from low-level hardware interfacing to handling
files and working with text data. Easy extensibility and integration was considered when
developing Python such that it can be easily integrated with existing applications—rich
application programming interfaces (APIs) can even be created to provide interfaces to
other applications and tools.

```
파이썬은 조숙한 최적화와 글쓰기보다 간단하고 아름다운 코드가 더 우아하고 사용하기 쉽다는 사실을 염두에 두고 디자인되었습니다.

해석하기 어려운 코드. 파이썬의 표준 라이브러리는 저수준 하드웨어 인터페이싱에서 핸들링에 이르기까지 다양한 기능과 기능을 갖춘 강력한 패키지입니다.

파일 및 텍스트 데이터 작업. Python을 개발할 때 기존 응용 프로그램과 쉽게 통합 될 수 있도록 손쉬운 확장 성 및 통합 성을 고려했습니다. 풍부한 응용 프로그램 프로그래밍 인터페이스 (API)를 만들어 다른 응용 프로그램 및 도구에 대한 인터페이스를 제공 할 수도 있습니다.
```

Python offers a lot of advantages and benefits. Here are some of the major benefits:

- Friendly and easy to learn: The Python programming language isextremely easy to understand and learn. Schools are starting topick up Python as the language of choice to teach kids to code.The learning curve is not very steep, and you can do a lot of funthings in Python, from building games to automating things

  like reading and sending email. (In fact, there is a popular bookand website dedicated to “automating the boring stuff” usingPython at https://automatetheboringstuff.com.) Python alsohas a thriving and helpful developer community, which makessure there is a ton of helpful resources and documentation outthere on the Internet. The community also organizes variousworkshops and conferences throughout the world.

- High-level abstractions: Python is a high-level language (HLL),where a lot of the heavy lifting needed by writing low level code iseliminated by high-level abstractions. Python has a sharp focuson code simplicity and extensibility, and you can perform variousoperations, simple or complex, in fewer lines of code than othertraditional compiled languages like C++ and C.

```
파이썬은 많은 장점과 이점을 제공합니다. 다음은 몇 가지 주요 이점입니다.

- 친숙하고 쉽게 배울 수 있습니다 : Python 프로그래밍 언어는 이해하기 쉽고 배우기 쉽습니다. 학교는 아이들에게 코드를 가르치기 위해 Python을 선택하는 언어로 시작하고 있습니다. 학습 곡선이 그리 가파르지는 않지만 게임을 작성하고 전자 메일을 읽고 보내는 것과 같은 자동화 작업에 이르기까지 Python에서 많은 즐거움을 얻을 수 있습니다. (사실, https://automatetheboringstuff.com에서 Python을 사용하여 "지루한 것들을 자동화"하는 데 사용되는 인기있는 bookand 웹 사이트가 있습니다.) Python은 번창하고 유용한 개발자 커뮤니티로서 많은 도움이되는 자료와 문서가 있습니다. 인터넷에서. 지역 사회는 또한 전세계의 다양한 워크샵과 컨퍼런스를 조직합니다.

- 상위 수준 추상화 : Python은 고수준 언어 (HLL)로, 저수준 코드를 작성하는 데 필요한 많은 양산 작업이 상위 수준 추상화에 의해 제거됩니다. 파이썬은 초점을 맞추는 코드의 단순성과 확장 성이 뛰어나며 C ++ 및 C와 같은 기존의 다른 컴파일 된 언어보다 적은 코드 행에서 단순하거나 복잡한 변수를 수행 할 수 있습니다.
```

- Boosts productivity: Python boosts productivity by reducing timetaken to develop, run, debug, deploy, and maintain large codebasescompared to other languages like Java, C++, and C. Large programsof more than a 100 lines can be reduced to 20 lines or less on averageby porting them to Python. High-level abstractions help developersfocus on the problem to be solved at hand rather than worry aboutlanguage-specific nuances. The hindrance of compiling and linkingis also bypassed with Python. Hence, Python is often the choice oflanguage especially when rapid prototyping and development areessential for solving an important problem in little time.

- Complete robust ecosystem: One of the main advantages of Python
  is that it is a multipurpose programming language that can be
  used for just about anything! From web applications to intelligent
  systems, Python powers a wide variety of applications and systems.
  We will talk about some of them later in this chapter. Besides being
  a multipurpose language, the wide variety of frameworks, libraries,
  and platforms that have been developed by using Python and to

  be used for Python form a complete robust ecosystem aroundPython. These libraries make life easier by giving us a wide variety ofcapabilities and functionality to perform various tasks with minimalcode. Some examples would be libraries for handling databases, textdata, machine learning, signal processing, image processing, deeplearning, artificial intelligence—and the list goes on.

- Open source: As open source, Python is actively developed andupdated constantly with improvements, optimizations, and newfeatures. Now the Python Software Foundation (PSF) owns allPython-related intellectual property (IP) and administers alllicense-related issues. Being open source has boosted the Pythonecosystem with almost all of its libraries also being open source, towhich anyone can share, contribute, and suggest improvementsand feedback. This helps foster healthy collaboration amongtechnologists, engineers, researchers, and developers.

- Easy to port, integrate, and deploy: Python is supported on all major operating systems (OS), including Linux, Windows,and macOS. Code written in one OS can easily be ported into another OS by simply copying the code files, and they will work seamlessly. Python can also be easily integrated and extended with existing applications and can interface with various APIs and devices using sockets, networks, and ports. Python can be used to invoke code for other languages, and there are Python bindings for invoking Python code from other languages. This helps in easy integration of Python code wherever necessary.
  The most important advantage, though, is that it is very easy to develop Python code and deploy it no matter how complex your codebase might be. If you follow the right continuous integration (CI) processes and manage your Python codebase properly, deployment usually involves updating your latest code and starting the necessary processes in your production environment. It is extremely easy to get proper working code in minimal time, which is often difficult to do with other languages.

```
- 생산성 향상 : Python은 Java, C ++ 및 C와 같은 다른 언어와 비교할 수있는 대형 코드베이스를 개발, 실행, 디버그, 배포 및 유지 관리하는 시간을 줄임으로써 생산성을 향상시킵니다. 100 개가 넘는 큰 프로그램은 20 개 줄 이하로 줄일 수 있습니다. averageby를 파이썬으로 포팅합니다. 높은 수준의 추상화는 개발자가 언어 별 뉘앙스에 대한 걱정보다 문제 해결에 집중할 수 있도록 도와줍니다. 컴파일과 링킹의 방해는 또한 파이썬으로 건너 뜁니다. 따라서 Python은 종종 빠른 프로토 타이핑과 개발이 중요한 문제를 해결하는 데 중요하지 않은 언어를 선택하는 경우가 많습니다.

- 완벽한 강력한 생태계 : 파이썬의 주요 장점 중 하나는 무엇이든 사용할 수있는 다용도 프로그래밍 언어입니다. 웹 응용 프로그램에서부터 지능형 시스템에 이르기까지 Python은 다양한 응용 프로그램과 시스템에 사용됩니다.
  우리는 이 장의 뒷부분에서 그들 중 일부에 대해서 이야기 할 것입니다. 다용도 언어 외에도 파이썬을 사용하고 파이썬에 사용하기 위해 개발 된 다양한 프레임 워크, 라이브러리 및 플랫폼은 파이썬에 대한 완벽한 견고한 생태계를 형성합니다. 이러한 라이브러리는 minimalcode로 다양한 작업을 수행 할 수있는 다양한 기능과 기능을 제공하여 작업을보다 쉽게 만듭니다. 예를 들어 데이터베이스, 텍스트 데이터, 기계 학습, 신호 처리, 이미지 처리, 인공 지능 저하 및 인공 지능을 다루는 라이브러리가 있으며 그 목록은 계속됩니다.

- 오픈 소스 : 오픈 소스로서 파이썬은 개선, 최적화 및 새로운 기능으로 지속적으로 개발되고 업데이트됩니다. 이제는 Python Software Foundation (PSF)이 모든 파이썬 관련 지적 재산 (IP)을 소유하고 모든 라이센스 관련 문제를 관리합니다. 오픈 소스이기 때문에 누구나 공유하고 개선하고 피드백을 제안하고 제안 할 수있는 거의 모든 라이브러리가 오픈 소스이기 때문에 파이썬 시스템을 향상 시켰습니다. 이를 통해 기술자, 엔지니어, 연구원 및 개발자 간의 건전한 협력을 촉진 할 수 있습니다.

- 쉽게 포팅, 통합 및 배포 : Python은 Linux, Windows 및 MacOS를 포함한 모든 주요 운영 체제 (OS)에서 지원됩니다. 한 OS에서 작성된 코드는 단순히 코드 파일을 복사하여 다른 OS에 쉽게 포팅 될 수 있으며 완벽하게 작동합니다. 파이썬은 기존 응용 프로그램과 쉽게 통합되고 확장 될 수 있으며 소켓, 네트워크 및 포트를 사용하여 다양한 API 및 장치와 인터페이스 할 수 있습니다. Python은 다른 언어의 코드를 호출하는 데 사용할 수 있으며 다른 언어의 Python 코드를 호출하는 Python 바인딩이 있습니다. 이는 필요할 때마다 Python 코드를 쉽게 통합하는 데 도움이됩니다.

하지만 가장 중요한 이점은 코드베이스가 얼마나 복잡하든 파이썬 코드를 개발하고 배포하는 것이 매우 쉽다는 것입니다. 올바른 연속 통합 (CI) 프로세스를 따르고 Python 코드베이스를 적절하게 관리하는 경우 배포에는 일반적으로 최신 코드를 업데이트하고 프로덕션 환경에서 필요한 프로세스를 시작해야합니다. 최소의 시간에 적절한 작업 코드를 얻는 것은 매우 쉽습니다. 이는 다른 언어로하기가 종종 어렵습니다.
```

All these features coupled with rapid strides in the application of Python in variouswidespread domains over the years have made Python extremely popular. Such has beenthe case that if the proper Python principles of simplicity, elegance, and minimalism arenot followed when writing code, the code is said to be not “pythonic.” There is a knownstyle and convention around writing good Python code, and lots of articles and booksteach how to write pythonic code. Active users and developers in the Python communitycall themselves Pythonistas, Pythoneers, and many more interesting names. The thrivingPython community makes the language all the more exciting since Python and its entireecosystem is always under active improvement and development.

```
이 모든 기능들은 지난 수년간 다양한 분야에서 파이썬을 사용하면서 급속도로 진보하여 파이썬을 대단히 인기있게 만들었습니다. 코드를 작성할 때 단순성, 우아함, 미니멀리즘 등의 적절한 파이썬 원칙이 따르지 않는다면 코드는 "파이썬 (Python)"이 아니라고 말합니다. 좋은 파이썬 코드를 작성하는 데 대한 알려진 스타일과 규칙이 있으며 많은 기사 pythonic 코드를 작성하는 법을 배우십시오. Python 커뮤니티의 적극적인 사용자와 개발자는 Pythonistas, Pythoneers 및 더 많은 흥미로운 이름을 갖습니다. 번성하는 파이썬 커뮤니티는 파이썬과 그 전체 시스템이 항상 적극적으로 개선되고 개발되고 있기 때문에 언어를 더욱 흥미롭게 만듭니다.
```



### The Zen of Python

You may be wondering what on earth the Zen of Python could be, but when you becomesomewhat familiar with Python, this is one of the first things you get to know. Thebeauty of Python lies in its simplicity and elegance. The Zen of Python is a set of 20guiding principles, or aphorisms, that have been influential in Python’s design. Long-time Pythoneer Tim Peters documented 19 of them in 1999, and they can be accessed

at https://hg.python.org/peps/file/tip/pep-0020.txt as a part of the PythonEnhancement Proposals (PEP) number 20 (PEP 20). The best part is, if you already havePython installed, you can access the Zen of Python at any time by running the followingcode in the Python or IPython shell:

```
In [5]: import this
The Zen of Python, by Tim Peters
```

```
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.

```

```
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

The above output showing the 19 principles that form the Zen of Python is included
in the Python language itself as an easter egg. The principles are written in simple English
and a lot of them are pretty self-explanatory, even if you have not written code before,
and many of them contain inside jokes! Python focuses on writing simple and clean
code that is readable. It also intends to make sure you focus a lot on error handling and
implementing code that is easy to interpret and understand. The one principle I would
most like you to remember is Simple is better than complex, which is applicable not only
for Python but for a lot of things when you are out there in the world solving problems.
Sometimes a simple approach beats a more complex one, as long as you know what you
are doing, because it helps you avoid overcomplicating things.

### Applications: When Should You Use Python?

Python, being a general and multipurpose programming language, can be used to buildapplications and systems for different domains and solve diverse real-world problems.Python comes with a standard library that hosts a large number of useful libraries andmodules that can be leveraged to solve various problems. Besides the standard library,thousands of third-party libraries are readily available on the Internet, encouraging opensource and active development. The official repository for hosting third-party librariesand utilities for enhancing development in Python is the Python Package Index (PyPI).Access it at https://pypi.python.org and check out the various packages. Currentlythere are over 80,000 packages you can install and start using.

Although Python can be used for solving a lot of problems, here are some of the most

popular domains:

- Scripting: Python is known as a scripting language. It can beused to perform many tasks, such as interfacing with networksand hardware and handling and processing files and databases,performing OS operations, and receiving and sending email.Python is also used extensively for server-side scripting and evenfor developing entire web servers for serving web pages. A lot

  of Python scripts are used in an ad-hoc fashion for automatingoperations like network socket communication, handling email,parsing and extracting web pages, file sharing and transfer viaFTP, communicating via different protocols, and several more.

- Web development: There are a lot of robust and stable Pythonframeworks out there that are used extensively for webdevelopment, including Django, Flask, Web2Py, and Pyramid.You can use them for developing complete enterprise webapplications, and Python supports various architecture styles likeRESTful APIs and the MVC architecture. It also provides ORMsupport to interact with databases and use OOP on top of that.Python even has frameworks like Kivy, which support cross-platform development for developing apps on multiple platformslike iOS, Android, Windows, and OS X. Python is also used fordeveloping rich internet applications (RIA) with the Silverlightframework support in IronPython, a Python version that is wellintegrated with the popular Microsoft .NET framework and pyjs,a RIA development framework supporting a Python-to-JavaScriptcompiler and an AJAX framework.

- Graphical user interfaces (GUIs): A lot of desktop-basedapplications with GUIs can be easily built with Python. Librariesand APIs like tkinter, PyQt, PyGTK, and wxPython allowdevelopers to develop GUI-based apps with simple as well ascomplex interfaces. Various frameworks enable developers todevelop GUI-based apps for different OSes and platforms.

- Systems programming: Being a high-level language, Python has
  a lot of interfaces to low-level OS services and protocols, and the
  abstractions on top of these services enable developers to write
  robust and portable system monitoring and administration tools.
  We can use Python to perform OS operations including creating,
  handling, searching, deleting, and managing files and directories.
  The Python standard library (PSL) has OS and POSIX bindings that
  can be used for handling files, multi-threading, multi-processing,
  environment variables, controlling sockets, pipes, and processes.
  This also enhances writing Python scripts for performing system-
  level administration tasks with minimal effort and lines of code.


- Database programming: Python is used a lot in connecting andaccessing data from different types of databases, be it SQL orNoSQL. APIs and connectors exist for these databases like MySQL,MSSQL, MongoDB, Oracle, PostgreSQL, and SQLite. In fact, SQLite,a lightweight relational database, now comes as a part of the Pythonstandard distribution itself. Popular libraries like SQLAlchemy andSQLObject provide interfaces to access various relational databasesand also have ORM components to help implement OOP-styleclasses and objects on top of relational tables.

- Scientific computing: Python really shows its flair for being
  multipurpose in areas like numeric and scientific computing. You
  can perform simple as well as complex mathematical operations
  with Python, including algebra and calculus. Libraries like
  SciPy and NumPy help researchers, scientists, and developers
  leverage highly optimized functions and interfaces for numeric
  and scientific programming. These libraries are also used as the
  base for developing complex algorithms in various domains like
  machine learning.

- Machine learning: Python is regarded as one of the most popularlanguages today for machine learning. There is a wide suite oflibraries and frameworks, like scikit-learn, h2o, tensorflow,theano, and even core libraries like numpy and scipy, for not onlyimplementing machine learning algorithms but also using themto solve real-world advanced analytics problems.

- Text analytics: As mentioned, Python can handle text data
  very well, and this has led to several popular libraries like
  nltk, gensim, and pattern for NLP, information retrieval, and
  text analytics. You can also apply standard machine learning
  algorithms to solve problems related to text analytics. This
  ecosystem of readily available packages in Python reduces time
  and efforts taken for development. We will be exploring several of
  these libraries in this book.

Even though the preceding list may seem a bit overwhelming, this is just scratchingthe surface of what is possible with Python. It is widely used in several other domainsincluding artificial intelligence (AI), game development, robotics, Internet of Things(IoT), computer vision, media processing, and network and system monitoring, just toname a few. To read some of the widespread success stories achieved with Python indifferent diverse domains like arts, science, computer science, education, and others,enthusiastic programmers and researchers can check out www.python.org/about/success/. To find out various popular applications developed using Python, seewww.python.org/about/apps/ and https://wiki.python.org/moin/Applications,where you will definitely find some applications you have used—some of them areindispensable.

CHAPTER 2 ■ PYTHON REFRESHER

57

CHAPTER 2 ■ PYTHON REFRESHER

### Drawbacks: When Should You Not Use Python?

I have been blowing the trumpet for Python till now, but you may be wondering are
there any drawbacks? Well, like any tool or language, Python has advantages and
disadvantages. Yes, even Python has some disadvantages, and here we will highlight
some of them so that you are aware of them when developing and writing code in Python:

- Execution speed performance: Performance is a pretty heavy term
  and can mean several things, so I’ll pinpoint the exact area to
  talk about and that is execution speed. Because Python is not a
  fully compiled language, it will always be slower than low-level
  fully compiled programming languages like C and C++. There
  are several ways you can optimize your code, including multi-
  threading and multi-processing. You can also use static typing
  and C extensions for Python (known as Cython). You can consider
  using PyPy also, which is much faster than normal Python since

  it uses a just-in-time (JIT) compiler (see http://pypy.org),but often, if you write well-optimized code, you can developapplications in Python just fine and do not need to depend onother languages. Remember that often the problem is not withthe tool but the code you write—something all developers andengineers realize with time and experience.

- Global Interpreter Lock (GIL): The GIL is a mutual exclusion lock
  used in several programming language interpreters, like Python
  and Ruby. Interpreters using GIL only allow one single thread
  to effectively execute at a time even when run on a multi-core
  processor and thus limit the effectively of parallelism achieved by
  multi-threading depending on whether the processes are I\O bound
  or CPU bound and how many calls it makes outside the interpreter.

- Version incompatibility: If you have been following Python news,
  you know that once Python released the 3.x version from 2.7.x,
  it was backward-incompatible in several aspects, and that has
  indeed opened a huge can of worms. Several major libraries and
  packages that had been built in Python 2.7.x started breaking
  when users unknowingly updated their Python versions. Hence, a
  large chunk of enterprises and the developer community still use
  Python 2.7.x due to legacy code and because newer versions of
  those packages and libraries were never built. Code deprecation
  and version changes are some of the most important factors in
  systems breaking down.

  Many of these issues are not specific to Python but apply to other languages too, soyou should not be discouraged from using Python just because of the preceding points—but you should definitely remember them when writing code and building systems.

58

### Python Implementations and Versions

There are several different implementations of Python and different versions of Pythonwhich are released periodically since it is under active development. This section discussesboth implementations and versions and their significance, which should give you someidea of which Python you might want to use for your development needs. Currently, thereare four major production-ready, robust, and stable implementations of Python:

- CPython is the regular old Python, which we know as just Python.
  It is both a compiler and interpreter and comes with its own
  set of standard packages and modules which were all written
  in standard C. This version can be used directly in all popular
  modern platforms. Most of the python third-party packages and
  libraries are compatible with this version.

- PyPy is a faster alternative Python implementation that uses
  a JIT compiler to make the code run faster than the CPython
  implementation—sometimes delivering speedups in the range of
  10x–100x. It is also more memory efficient, supporting greenlets
  and stackless for high parallelism and concurrency.

- Jython is a Python implementation for the Java platform
  supporting Java Virtual Machine (JVM) for any version of
  Java ideally above version 7. Using Jython you can write code
  leveraging all types of Java libraries, packages, and frameworks.
  It works best when you know more about the Java syntax and
  the OOP principles that are used extensively in Java, like classes,
  objects, and interfaces.

- IronPython is the Python implementation for the popularMicrosoft .NET framework, also termed as the CommonLanguage Runtime (CLR). You can use all of Microsoft’s CLRlibraries and frameworks in IronPython, and even though you donot essentially have to write code in C#, it is useful to know moreabout syntax and constructs for C# to use IronPython effectively.

  To start with I would suggest you to use the default Python which is the CPythonimplementation, and experiment with the other versions only if you are really interested ininterfacing with other languages like C# and Java and need to use them in your codebase.

  There are two major versions: the 2.x series and the 3.x series, where x is a number.
  Python 2.7 was the last major version in the 2.x series, released in 2010. From then on,
  future releases have included bug fixes and performance improvements but no new
  features. The latest version is Python 2.7.12, released in June 2016. The 3.x series started
  with Python 3.0, which introduced many backward-incompatible changes compared
  to Python 2.x. Each version 3 release not only has bug fixes and improvements but also
  introduces new features, such as the AsyncIO module released recently. As of this writing,
  Python 3.5.2 is the latest version in the 3.x series, released in June 2016.

CHAPTER 2 ■ PYTHON REFRESHER

59

CHAPTER 2 ■ PYTHON REFRESHER

There are many arguments over which version of Python should be used. We
will discuss some of them later on, but the best way to go about thinking about it is to
consider what problem is to be solved and the entire software ecosystem you will need
to use for that, starting from libraries, dependencies, and architecture to implementation
and deployment—and also considering things like reusing existing legacy codebases.

## Installation and Setup

Now that you have been acquainted with Python and know more about the language,its capabilities, implementations, and versions, we will be talking about which versionof Python we will be using in the book and also discussing details on how to set up yourdevelopment environment and handle package management and virtual environments.This section will give you a good head start on getting things ready for following alongwith the various hands-on examples we will be covering in this book.

```
이제는 파이썬에 대해 잘 알고 있고 언어, 기능, 구현 및 버전에 대해 더 많이 알고 있기 때문에이 책에서 사용할 버전의 Python과 개발 환경 설정 방법에 대한 자세한 내용과 패키지 관리 및 가상 환경을 다루십시오.이 섹션에서는이 책에서 다룰 실습 예제를 따라 할 준비를 갖추는 데 앞장설 것입니다.
```

### Which Python Version?

The two major Python versions, as mentioned, are the 2.x series and the 3.x series. They
are quite similar, although there have been several backward-incompatible changes in
the 3.x version, which has led to a huge drift between people who use 2.x and people
who use 3.x. Most legacy code and a large majority of Python packages on PyPI were
developed in Python 2.7.x, and many package owners do not have the time or will to port
all their codebases to Python 3.x, since the effort required would not be minimal. Some of
the changes in 3.x are as follows:

- All text strings are Unicode by default.

- print and exec are now functions and no longer statements.

- range() returns a memory-efficient iterable and not a list.

- The style for classes has changed.

- Library and name changes are based on convention and styleviolations.

```
앞서 언급 한 두 가지 주요 Python 버전은 2.x 시리즈와 3.x 시리즈입니다. 그것들은 3.x 버전에서 몇 가지 하위 호환되지 않는 변경 사항이 있었지만 2.x를 사용하는 사람들과 3.x를 사용하는 사람들 사이에 큰 차이를 가져 오게했습니다. Python의 대부분의 레거시 코드와 대부분의 Python 패키지는 Python 2.7.x에서 개발되었으며 많은 패키지 소유자는 필요한 모든 노력이 최소화되지 않았기 때문에 모든 코드 기반을 Python 3.x로 이식 할 시간이나 의지가 없습니다.  
3.x의 변경 사항 중 일부는 다음과 같습니다.

- 모든 텍스트 문자열은 기본적으로 유니 코드입니다.
- 이제 print와 exec는 함수이며 더 이상 명령문이 아닙니다.
- range ()는 목록이 아닌 메모리 효율적인 iterable을 반환합니다.
- 클래스 스타일이 변경되었습니다.
- 도서관 및 이름 변경은 국제 대회 및 스타일 위반에 근거합니다.
```

To know more about changes introduced since Python 3.0, check https://docs.python.org/3/whatsnew/3.0.html, the official documentation listing the changes. Thatlink should give you a pretty good idea of what changes can break your code if you areporting it from Python 2 to Python 3.

```
Python 3.0 이후에 도입 된 변경 사항에 대한 자세한 내용을 보려면 https://docs.python.org/3/whatsnew/3.0.html을 확인하십시오. Thatlink는 파이썬 2에서 파이썬 3으로 변경하는 경우 코드가 변경 될 수 있다는 것을 잘 알고 있습니다.
```

As for the problem of selecting which version, there is no absolute answer for this.It purely depends on the problem you are trying to solve and the current code andinfrastructure you have and how you will be maintaining this code in the future alongwith all its necessary dependencies. If you are starting a new project completely andhave a fairly good idea that you do not need any external packages and libraries that aresolely dependent on Python 2.x, you can go ahead with Python 3.x and start developingyour system. But if you have a lot of dependencies on external packages that might breakwith Python 3.x or that are available for only Python 2.x, you have no choice but to stickwith Python 2.x. Besides that, often you have to deal with legacy code that’s been around a long time, especially in large companies and organizations that have huge codebases.In that case, porting the whole code to Python 3.x would be wasted effort—kind of re-inventing the wheel, since you are not missing out on major functionality and capabilitiesby using Python 2.x, and in fact you might even end up breaking the existing code andfunctionality without even realizing it. In the end, this is a decision left to you, the reader,which you must make carefully considering all scenarios.

```
어떤 버전을 선택해야할지에 대한 절대적인 대답은 없습니다. 이것은 당신이 해결하고자하는 문제와 현재 가지고있는 코드 및 인프 라 스트럭처와 앞으로 필요한 모든 코드와 함께이 코드를 어떻게 유지할 것인지에 달려 있습니다. 의존성. 새로운 프로젝트를 완전히 시작하고 Python 2.x에 의존적 인 외부 패키지와 라이브러리가 필요 없다는 좋은 아이디어가 있다면 Python 3.x로 가서 시스템을 개발할 수 있습니다. 그러나 Python 3.x와 깰 수 있거나 Python 2.x에서만 사용할 수있는 외부 패키지에 많은 의존성이 있다면 Python 2.x를 고수 할 수 밖에 없습니다. 그 외에도 커다란 코드베이스를 가진 대기업이나 조직에서 오랫동안 사용해온 레거시 코드를 처리해야하는 경우가 종종 있습니다.이 경우 전체 코드를 Python 3.x로 포팅하는 것은 낭비 될 것입니다. Python 2.x를 사용하여 주요 기능과 성능을 놓치지 않고 기존 코드와 기능을 깨닫지 못하게 될 수도 있기 때문에 휠을 개척해야합니다. 결국 이것은 모든 시나리오를 신중하게 고려해야하는 독자, 독자의 결정입니다.
```

We will be using Python 2.7.11 in this book just to be on the safe side, since it is a tried
and tested version of Python in all major enterprises. You are most welcome to follow
along even in Python 3.x—the algorithms and techniques will be the same, although
you may have to take into account changes, such as the fact that the print statement is a
function in Python 3.x and so on.

```
우리는이 책에서 Python 2.7.11을 모든 주요 기업에서 시험되고 검증 된 Python 버전이기 때문에 안전한면에있을 것입니다.
Python 3.x 에서조차 따라하기를 환영합니다. 알고리즘과 기술은 동일 할 것입니다. 그러나 print 문이 Python 3.x의 함수이고, 곧.
```



### Which Operating System?

There are several popular OSes out there, and everybody has their own preference. Thebeauty of Python is that is can run seamlessly on any OS without much hassle. The threemost popular OSes include the following:

- Windows

- Linux

- OS X (now known as macOS)

You can choose any OS of your choice and use it for following along with the
examples in this book. We will be using Windows as the primary OS in this book.
This book is aimed at working professionals and practitioners, most of whom in their
enterprise environment usually use the enterprise version of Windows. Besides that,
several Python external packages are really easy to install on a UNIX-based OS like Linux
and macOS. However, sometimes there are major issues in installing them for Windows,
so I want to highlight such instances and make sure to address them such that executing
any of the code snippets and samples here becomes easy for you. But again, you are most
welcome to use any OS of your choice when following the examples in this book.

```
거기에 몇 가지 인기있는 OSes가 있으며, 모두가 자신의 취향이 있습니다. 파이썬의 매력은 모든 번거 로움없이 모든 OS에서 완벽하게 실행할 수 있다는 것입니다. 세 번째로 인기있는 OS에는 다음이 포함됩니다.

- Windows
- 리눅스
- OS X (현재 macOS라고 함)

원하는 OS를 선택하고이 책의 예와 함께 사용할 수 있습니다. 이 책에서는 Windows를 기본 운영 체제로 사용합니다.
이 책은 실무 전문가 및 실무자를 대상으로하며 대부분 엔터프라이즈 환경에서 일반적으로 엔터프라이즈 버전의 Windows를 사용합니다. 게다가 여러 Python 외부 패키지는 Linux 및 macOS와 같은 UNIX 기반 OS에 설치하기 쉽습니다. 그러나 때로는 Windows 용으로 설치하는 데 중요한 문제가 있으므로 이러한 인스턴스를 강조 표시하여 여기에서 코드 스 니펫과 샘플을 실행하면 쉽게 해결할 수 있습니다. 그러나 다시 한번,이 책의 예를 따를 때 원하는 OS를 사용하는 것이 가장 좋습니다.
```

### Integrated Development Environments

Integrated development environments (IDEs) are software products that enable
developers to be highly productive by providing a complete suite of tools and capabilities
necessary for writing, managing, and executing code. The usual components of an
IDE include source editor, debugger, compiler, interpreter, and refactoring and build
tools. They also have other capabilities such as code-completion, syntax highlighting,
error highlighting and checks, objects, and variable explorers. IDEs can be used to
manage entire codebases—much better than trying to write code in a simple text
editor, which takes more time. That said, experienced developers often use simple
plain text editors to write code, especially if they are working in server environments.
You’ll find a list of IDEs used specially for Python at https://wiki.python.org/moin/
IntegratedDevelopmentEnvironments.

We will be using the Spyder IDE, which comes with the Anaconda Pythondistribution for writing and executing our code.

This section covers details regarding how to set up your Python environment withminimal effort and the main components required.

First, head over to the official Python website and download Python 2.7.11 from
www.python.org/downloads/. Or download a complete Python distribution with over
700 packages, known as the Anaconda Python distribution, from Continuum Analytics,
which is built specially for data science and analytics, at www.continuum.io/downloads.
This package provides a lot of advantages, especially for Windows users, where installing
some of the packages like numpy and scipy can sometimes cause issues. You can get more
information about Anaconda and Continuum Analytics at https://docs.continuum.io/
anaconda/index. Anaconda comes with conda, an open source package and environment
management system, and Spyder (Scientific Python Development Environment), an IDE
for writing and executing your code.

For other OS options, check out the relevant instructions on the website.

Once you have Python downloaded, start the executable and follow the instructionson the screen, clicking the Next button at each stage. But before starting the installation,remember to check the two options shown in Figure 2-1.

Figure2-1. InstallingtheAnacondaPythondistribution



Once the installation is complete, either start up Spyder by double-clicking therelevant icon or start the Python or IPython shell from the command prompt. Spyderprovides a complete IDE to write and execute code in both the regular Python andIPython shell. Figure 2-2 shows how to run IPython from the command prompt.

Figure2-2. StartingIPythonfromthecommandprompt

Figure 2-2 depicts printing a regular sentence saying Welcome to Python! just to showyou that Python is properly installed and working fine. The input and output executionhistory are kept in variables called In and Out, indicated in the figure by the promptnumbers, such as In[1]. IPython provides a lot of advantages including code completion,inline executions and plots, and running code snippets interactively. We will be runningmost of our snippets in the IPython shell just like the examples seen in Chapter 1.

Now that you have Anaconda installed, you are ready to start running the codesamples in this book. Before we move on to the next section, I want to cover packagemanagement briefly. You can use either the pip or conda commands to install, uninstall,and upgrade packages. The shell command shown in Figure 2-3 depicts installing thepandas library via pip. Because we already have the library installed, you can use the--upgrade flag as shown in the figure.

CHAPTER 2 ■ PYTHON REFRESHER

Figure2-3. Packagemanagementusingpip

63

CHAPTER 2 ■ PYTHON REFRESHER

The conda package manager is better than pip in several aspects because it providesa holistic view of which dependencies are going to be upgraded and the specific versionsand other details during installation. Also pip often fails to install some packages inWindows, but conda has no such issues during installation. Figure 2-4 depicts how tomanage packages using conda.

Figure2-4. Packagemanagementusingconda

Now you have a much better idea of how to install external packages and libraries inPython. This will be useful later when we install some libraries that have been specificallybuilt for text analytics. Your Python environment should now be set up and ready forexecuting code. Before we dive into the basic and advanced concepts in Python, we willconclude this section with a discussion about virtual environments.

### Virtual Environments

A virtual environment, or venv, is a complete isolated Python environment with its ownPython interpreter, libraries, modules, and scripts. This environment is a standaloneenvironment isolated from other virtual environments and the default system-levelPython environment. Virtual environments are extremely useful when you have multipleprojects or codebases that have dependencies on different versions of the same packagesor libraries. For example, if my project TextApp1 depends on nltk 2.0 and anotherproject, TextApp2, depends on nltk 3.0, then it would be impossible to run both projectson the same system. Hence, the need for virtual environments that provide completeisolated environments that can be activated and deactivated as needed.

64

CHAPTER 2 ■ PYTHON REFRESHERTo set up a virtual environment, you need to install the virtualenv package as follows:

```
E:\Apress>pip install virtualenv
Collecting virtualenv

```

```
  Downloading virtualenv-15.0.2-py2.py3-none-any.whl (1.8MB)
    100% |################################| 1.8MB 290kB/s
```

```
Installing collected packages: virtualenv
Successfully installed virtualenv-15.0.2

```

Once installed, you can create a virtual environment as follows, where we create a newproject directory called test_proj and create the virtual environment inside the directory:

```
E:\Apress>mkdir test_proj && chdir test_proj
E:\Apress\test_proj>virtualenv venv
New python executable in E:\Apress\test_proj\venv\Scripts\python.exe
Installing setuptools, pip, wheel...done.

```

Once you have installed the virtual environment successfully, you can activate itusing the following command:

```
E:\Apress\test_proj>venv\Scripts\activate
(venv) E:\Apress\test_proj>python --version
Python 2.7.11 :: Continuum Analytics, Inc.

```

For other OS platforms, you may need to use the command source venv/bin/activate to activate the virtual environment.

Once the virtual environment is active, you can see the (venv) notation as shown inthe preceding code output, and any new packages you install will be placed in the venvfolder in complete isolation from the global system Python installation. This differenceis illustrated by depicting different versions for the pandas package in the global systemPython and the virtual environment Python in the following code:

```
C:\Users\DIP.DIPSLAPTOP>echo 'This is Global System Python'
'This is Global System Python'
C:\Users\DIP.DIPSLAPTOP>pip freeze | grep pandas
pandas==0.18.0

```

```
(venv) E:\Apress\test_proj>echo 'This is VirtualEnv Python'
'This is VirtualEnv Python'
(venv) E:\Apress\test_proj>pip install pandas
Collecting pandas

```

```
  Downloading pandas-0.18.1-cp27-cp27m-win_amd64.whl (6.2MB)
    100% |################################| 6.2MB 142kB/s

```

```
Installing collected packages: pandas
Successfully installed pandas-0.18.1
(venv) E:\Apress\test_proj>pip freeze | grep pandas
pandas==0.18.1

```

65

CHAPTER 2 ■ PYTHON REFRESHER

You can see from that code how the pandas package has different versions in thesame machine: 0.18.0 for global Python and 0.18.1 for the virtual environment Python.Hence, these isolated virtual environments can run seamlessly on the same system.

Once you have finished working in the virtual environment, you can deactivate itagain as follows:

```
(venv) E:\Apress\test_proj>venv\Scripts\deactivate
E:\Apress\test_proj>

```

This will bring you back to the system’s default Python interpreter with all itsinstalled libraries. This gives us a good idea about the utility and advantages of virtualenvironments, and once you start working on several projects, you should definitelyconsider using it. To find out more about virtual environments, check out http://docs.python-guide.org/en/latest/dev/virtualenvs/, the official documentation for thevirtualenv package.

This brings us to the end of our installation and setup activities, and now we willbe looking into Python concepts, constructs, syntax, and semantics using hands-onexamples.

## Python Syntax and Structure

There is a defined hierarchical syntax for Python code that you should remember whenwriting code. Any big Python application or system is built using several modules, whichare themselves comprised of Python statements. Each statement is like a command ordirection to the system directing what operations it should perform, and these statementsare comprised of expressions and objects. Everything in Python is an object—includingfunctions, data structures, types, classes and so on. This hierarchy is visualized in

Figure 2-5.

![ddd](http://1.bp.blogspot.com/-F70Jpp_GrGM/WcVO3Wak9RI/AAAAAAAAEg0/4qtsSOtB-fwcVwVI584D_N_Dq7j195FpACK4BGAYYCw/s1600/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA%2B2017-09-23%2B02.56.03.png)

The basic statements consist of objects, expressions which usually make use of objectsand process and perform operations on them. Objects can be anything from simple datatypes and structures to complex objects, including functions and reserved words that havetheir own specific roles. Python has around 37 keywords, or reserved words, which havetheir own designated roles and functions. Table 2-1 list each keyword in detail, includingexamples that should be useful and handy when you are using them in your code.

Table2-1. PythonReservedWords

![ddd](http://4.bp.blogspot.com/-ZTYafkk2-Ko/WcVPVFYczKI/AAAAAAAAEg8/F4pW3PjgIdw9KZjrI8JD1UOjrsxOZ142ACK4BGAYYCw/s1600/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA%2B2017-09-23%2B02.58.26.png)

![aaa](http://2.bp.blogspot.com/-JdnWWhVOpyU/WcVNzbuBNSI/AAAAAAAAEgo/zCjtu7FS_yQuVsREa42mnMyRWH357AMFwCK4BGAYYCw/s1600/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA%2B2017-09-23%2B02.51.20.png)

Table 2-1 shows us all of Python’s keywords that are used in statements. However,
there are a few caveats to remember. The async and await keywords are only available
in Python 3.5.x onwards. The exec and print keywords are statements only in Python
2.x—starting from Python 3.x they are functions. The keywords False, True, and nonlocal
were introduced starting with Python 3.x in the keywords list.

```
표 2-1은 명령문에 사용 된 모든 Python 키워드를 보여줍니다. 그러나 기억해야 할 몇 가지주의 사항이 있습니다. async 및 await 키워드는 Python 3.5.x 이상에서만 사용할 수 있습니다. exec 및 print 키워드는 Python 2.x에서만 사용되는 문장입니다. Python 3.x부터는 함수입니다. False, True 및 nonlocal 키워드는 키워드 목록에서 Python 3.x부터 도입되었습니다.
```

Python statements usually direct the interpreter as to what they should do whenexecuting the statements. A bunch of statements usually forms a logical block of code.Various constructs including functions and loops and conditionals help in segregatingand executing blocks of code using logic and design based on user decisions. Python alsofocuses a lot on readability—hence, indentation is an important part of Python code. Bydefault, Python does not use punctuation like semicolons to indicate end of statements. Italso uses tabs or whitespaces to indicate and delimit specific blocks of code instead of thetraditional braces or keywords as used in languages like C, C++, Java, and so on. Python accepts both spaces and tabs as indentation, with the usual norm being one tab or fourspaces to indicate each specific block of code. Unindented code will always throw syntaxerrors, so anyone writing Python code must be extra careful with code formatting andindentation.

```
파이썬 서술문은 대개 서술문을 실행할 때 어떻게해야하는지 인터프리터에게 지시합니다. 일련의 명령문은 일반적으로 논리적 블록의 코드를 형성합니다. 함수와 루프 및 조건문을 비롯한 다양한 구성 요소는 사용자 결정을 기반으로 한 논리 및 디자인을 사용하여 코드 블록을 분리하고 실행하는 데 도움이됩니다. 파이썬은 가독성에 많은 관심을 가지고 있습니다. 따라서 들여 쓰기는 파이썬 코드의 중요한 부분입니다. 기본적으로 파이썬은 문장의 끝을 나타내는 세미콜론 같은 구두점을 사용하지 않습니다. 또한 탭이나 공백을 사용하여 C, C ++, Java 등과 같은 언어에서 사용되는 기존의 중괄호 또는 키워드 대신 특정 코드 블록을 지정하고 구분합니다. 파이썬은 공백과 탭을 모두 들여 쓰기로 받아들입니다. 통상적 인 규범은 코드의 각 특정 블록을 나타 내기위한 하나의 탭이나 네 공간입니다. 인 코드되지 않은 코드는 항상 syntaxerrors를 발생 시키므로 파이썬 코드를 작성하는 사람은 코드 형식화 및 색인에주의해야합니다.
```

Python programs are usually structured around the hierarchy mentioned earlier.
Each module is usually a directory with a __init__.py file, which makes the directory a package, and it may have multiple modules, each of which is an individual Python(.py) file. Each module usually has classes and objects like functions that are invoked by other modules and code. All interconnected modules finally make up a complete Pythonprogram, application, or system. Usually you start any project by writing necessary code in Python (.py) files and making it modular as it gets bigger by adding more components.

```
파이썬 프로그램은 일반적으로 앞에서 언급 한 계층 구조를 기반으로 구성됩니다.
각 모듈은 일반적으로 디렉토리를 패키지로 만드는 init.py 파일이있는 디렉토리이며, 각 모듈은 개별 Python (.py) 파일 인 여러 모듈을 포함 할 수 있습니다. 각 모듈에는 일반적으로 다른 모듈 및 코드에 의해 호출되는 함수와 같은 클래스 및 객체가 있습니다. 모든 상호 연결된 모듈은 마침내 완벽한 파이썬 프로그램, 응용 프로그램 또는 시스템을 구성합니다. 일반적으로 필요한 코드를 Python (.py) 파일로 작성하고 더 많은 구성 요소를 추가하여 더 커지면서 모듈화되도록하여 프로젝트를 시작합니다.
```



## Data Structures and Types

Python has several data types and many are used as data structures for handling data. Alldata types are derived from the default object data type in Python. This object data typeis an abstraction used by Python for managing and handling data. Code and data are allstored and handled by objects and relations among objects. Each object has three thingsor properties that distinguish it from other objects:

- Identity: This is unique and never changes once the object iscreated and is usually represented by the object’s memoryaddress.
- Type: This determines the type of object (usually the data type,which is again a child of the base object type).
- Value: The actual value stored by the object.
  Let’s say a variable is holding a string that is one of the data types. To see the three properties in action, you can use the functions depicted in the following code snippet:

```
파이썬에는 여러 가지 데이터 유형이 있으며 많은 것은 데이터 처리를 위한 데이터 구조로 사용됩니다. Alldata 유형은 Python의 기본 오브젝트 데이터 유형에서 파생됩니다. 이 객체 데이터 유형은 데이터를 관리하고 처리하기 위해 파이썬에서 사용되는 추상화입니다. 코드와 데이터는 객체와 객체 간의 관계에 의해 모두 저장되고 처리됩니다. 각 객체는 다른 객체와 구별되는 세 가지 속성 또는 속성을가집니다.

- Identity : 이것은 고유하고 개체가 만들어지면 변경되지 않으며 대개 개체의 memoryaddress로 나타납니다.
- Type : 객체 유형을 결정합니다 (일반적으로 기본 객체 유형의 하위 인 데이터 유형).
- Value : 개체에 의해 저장된 실제 값입니다.
   변수가 데이터 유형 중 하나 인 문자열을 보유하고 있다고 가정 해 봅시다. 세 가지 속성을 확인하려면 다음 코드 스 니펫에 설명 된 함수를 사용할 수 있습니다.
```

```
In [46]: new_string = "This is a String"  # storing a string
In [47]: id(new_string)  # shows the object identifier (address)
Out[47]: 243047144L
In [48]: type(new_string)  # shows the object type
Out[48]: str
In [49]: new_string  # shows the object value
Out[49]: 'This is a String'
```

Python has several data types, including several core data types and complex onesincluding functions and classes. In this section we will talk about the core data types ofPython, including some that are used extensively as data structures to handle data. Thesecore data types are as follows:

- Numeric

- Strings

- Lists

- Sets

- Dictionaries

- Tuples

- Files

- Miscellaneous

Although that’s not an exhaustive list, more than 90 percent of your time will bespent writing Python statements that make use of these objects. Let’s discuss each ofthem in more detail to understand their properties and behavior better.

```
파이썬에는 몇 가지 핵심 데이터 유형과 함수 및 클래스를 포함하는 복잡한 데이터 유형이 포함 된 여러 데이터 유형이 있습니다. 이 섹션에서는 파이썬의 핵심 데이터 유형에 대해 설명하고 데이터를 처리하기위한 데이터 구조로 광범위하게 사용되는 일부 유형을 포함합니다. 두 번째 데이터 유형은 다음과 같습니다.

- 숫자
- 문자열
- 목록
- 세트
- 사전
- 튜플
- 파일
- 기타

이것이 전체 목록은 아니지만, 90 % 이상이 이러한 객체를 사용하는 Python 문을 작성하는 데 별 도움이되지 않습니다. 그들의 속성과 행동을 더 잘 이해하기 위해 각각의 주제를보다 자세히 논의합시다.
```



### Numeric Types

The numeric data type is perhaps the most common and basic data type in Python. Allkinds of applications end up processing and using numbers in some form or the other.There are mainly three numeric types: integers, floats, and complex numbers. Integers arenumbers that do not have a fractional part or mantissa after the decimal point. Integerscan be represented and operated upon as follows:

```
숫자 데이터 유형은 아마도 Python에서 가장 보편적이며 기본적인 데이터 유형입니다. 모든 종류의 응용 프로그램은 일부 형식 또는 다른 형식으로 숫자를 처리하고 사용합니다. 정수, 부동 소수점 및 복소수는 주로 세 가지 숫자 유형이 있습니다. 정수는 소수점 이하의 소수부 또는 가수가없는 수입니다. 정수는 다음과 같이 나타낼 수 있습니다 :
```

```
In [52]: # representing integers and operations on them
In [53]: num = 123
```

```
In [54]: type(num)
Out[54]: int
```

```
In [55]: num + 1000  # addition
Out[55]: 1123
```

```
In [56]: num * 2  # multiplication
Out[56]: 246
```

```
In [59]: num /  2  # integer division
Out[59]: 61
```

There are also various types of integers, depending on their radix or base. Theseinclude decimal, binary, octal, and hexadecimal integers. Normal nonzero leadingsequences of numbers are decimal integers. Integers that start with a 0, or often 0o toprevent making mistakes, are octal integers. Numbers that start with 0x are hexadecimal,and those starting with 0b are binary integers. You can also make use of the bin(), hex(),and oct() functions for converting decimal integers to the respective base form.

The following code snippet illustrates the various forms of integers:

```
또한 기수 나 기수에 따라 다양한 유형의 정수가 있습니다. 여기에는 10 진수, 2 진수, 8 진수 및 16 진수가 포함됩니다. 
숫자의 일반적인 0이 아닌 선행 열은 10 진수입니다. 정수로 시작하는 정수는 0 또는 실수를 방지하기 위해 8 진 정수입니다. 
0x로 시작하는 숫자는 16 진수이고 0b로 시작하는 숫자는 2 진 정수입니다. 

bin (), hex () 및 oct () 함수를 사용하여 10 진 정수를 해당 기본 형식으로 변환 할 수도 있습니다.

다음 코드 스 니펫은 다양한 형태의 정수를 보여줍니다.
```

```
In [94]: # decimal
In [95]: 1 + 1
Out[95]: 2
```

```
In [96]: # binary
In [97]: bin(2)
Out[97]: '0b10'
In [98]: 0b1 + 0b1
Out[98]: 2
```

```
In [99]: bin(0b1 + 0b1)
Out[99]: '0b10'
```

```
In [100]: # octal
In [101]: oct(8)
Out[101]: '010'
In [102]: oct(07 + 01)
Out[102]: '010'
```

```
In [103]: 0o10
Out[103]: 8
```

```
In [104]: # hexadecimal
In [105]: hex(16)
Out[105]: '0x10'
In [106]: 0x10
Out[106]: 16
```

```
In [116]: hex(0x16 + 0x5)
Out[116]: '0x1b'

```

Floating point numbers, or floats, are represented as a sequence of numbers thatinclude a decimal point and some numbers following it (the mantissa), an exponent part(e or E followed by a +/- sign followed by digits), or sometimes both of them. Here aresome examples of floating point numbers:

```
부동 소수점 수 또는 부동 소수점은 소수점과 그 뒤에 나오는 일부 숫자 (가수), 지수 부분 (e 또는 E와 +/- 부호 다음에 숫자가 오는) 또는 때때로 둘 다 포함하는 숫자의 시퀀스로 표시됩니다 그들의. 부동 소수점 숫자의 예는 다음과 같습니다.
```

```
In [126]: 1.5 + 2.6
Out[126]: 4.1

```

```
In [127]: 1e2 + 1.5e3 + 0.5
Out[127]: 1600.5
```

```
In [128]: 2.5e4
Out[128]: 25000.0
```

```
In [129]: 2.5e-2
Out[129]: 0.025

```

The floating point numbers have a range and precision similar to the double datatype in the C language.

Complex numbers have two components, a real and an imaginary componentrepresented by floating point numbers. The imaginary literal consists of the numberfollowed by the letter j, and this symbol j at the end of the literal indicates the square rootof –1. The following code snippet shows some representations and operations of complexnumbers:

```
부동 소수점 숫자의 범위와 정밀도는 C 언어의 double 데이터 유형과 비슷합니다.

복소수에는 부동 소수점 숫자로 표현 된 실수 및 허수 성분의 두 가지 구성 요소가 있습니다. 가상의 리터럴은 문자 j에 이어지는 숫자로 구성되며 리터럴 끝에있는이 기호 j는 제곱근 -1을 나타냅니다. 다음 코드 스 니펫은 complexnumber의 표현과 연산을 보여줍니다.
```

```
In [132]: cnum = 5 + 7j
```

```
In [133]: type(cnum)
Out[133]: complex
```

```
In [134]: cnum.real
Out[134]: 5.0
```

```
In [135]: cnum.imag
Out[135]: 7.0
```

```
In [136]: cnum + (1 - 0.5j)
Out[136]: (6+6.5j)
```

### Strings

Strings are sequences or collections of characters used to store and represent textual
data—which will be our data type of choice in most examples in the book. Strings can
be used to store both textual as well as bytes as information. Strings have a wide variety
of methods that can be used for handling and manipulating strings, which we will see in
detail later in this chapter. An important point to remember is that strings are immutable,
and any operations performed on strings always creates a new string object (remember
the three properties of an object?) rather than just mutating and changing the value of the
existing string object.

The following code snippet shows some string representations and some basicoperations on strings:

```
문자열은 텍스트를 저장하고 표현하는 데 사용되는 문자의 시퀀스 또는 모음입니다.
데이터 -이 책의 대부분의 예제에서 우리가 선택한 데이터 유형이 될 것입니다. 문자열은 텍스트뿐만 아니라 바이트를 정보로 저장하는 데 사용될 수 있습니다. 문자열에는 문자열 처리 및 조작에 사용할 수있는 다양한 메서드가 있습니다. 자세한 내용은이 장의 뒷부분에서 설명합니다. 기억해야 할 중요한 점은 문자열이 변경되지 않으며 문자열에서 수행되는 모든 작업은 기존 문자열 개체의 값을 변경하고 변경하는 것이 아니라 항상 새 문자열 개체를 만듭니다 (개체의 세 가지 속성을 기억해야합니다).

다음 코드 스니 j은 일부 문자열 표현과 문자열에 대한 일부 기본 조작을 보여줍니다.
```

```
In [147]: s1 = 'this is a string'
In [148]: s2 = 'this is "another" string'
In [149]: s3 = 'this is the \'third\' string'
In [150]: s4 = """this is a
     ...: multiline
     ...: string"""
In [151]: print s1, s2, s3, s4
this is a string this is "another" string this is the 'third'
string this is a multiline string
In [152]: print s3 + '\n' + s4
this is the 'third' string
this is a
multiline string
In [153]: ' '.join([s1, s2])
Out[153]: 'this is a string this is "another" string'
In [154]: s1[::-1]  # reverses the string
Out[154]: 'gnirts a si siht
```

### Lists

Lists are collections of arbitrary heterogeneous or homogenous typed objects. Lists alsofollow a sequence based on the order in which the objects are present in the list, andeach object has its own index with which it can be accessed. Lists are similar to arrays inother languages, with the distinction that unlike arrays, which hold homogenous itemsof the same type, lists can contain different types of objects. A simple example would bea list containing numbers, strings, and even sublists. If a list contains objects that are liststhemselves, these are often called nested lists.

The following code snippet shows some examples of lists:

```
목록은 임의의 이기종 또는 동질 유형 개체의 모음입니다. 또한 목록은 개체가 목록에있는 순서에 따라 순서를 따르고 각각의 개체는 액세스 할 수있는 자체 색인을 가지고 있습니다. 리스트는 다른 언어의 배열과 유사합니다. 동일한 유형의 동일한 항목을 보유하는 배열과는 달리 목록에는 여러 유형의 객체가 포함될 수 있습니다. 간단한 예제는 숫자, 문자열 및 심지어 하위 목록을 포함하는 목록입니다. 목록에 목록이있는 개체가 목록에 포함되어 있으면 이러한 목록을 종종 중첩 목록이라고합니다.

다음 코드 스니 j은 목록의 일부 예를 보여줍니다.
```

```Python
In [161]: l1 = ['eggs', 'flour', 'butter']
In [162]: l2 = list([1, 'drink', 10, 'sandwiches', 0.45e-2])
In [163]: l3 = [1, 2, 3, ['a', 'b', 'c'], ['Hello', 'Python']]
In [164]: print l1, l2, l3
['eggs', 'flour', 'butter'] [1, 'drink', 10, 'sandwiches', 0.0045] [1, 2, 3,
['a', 'b', 'c'], ['Hello', 'Python']]
```

You can also perform numerous operations on lists, including indexing, slicing,appending, popping, and many more. Some typical operations on lists are depicted in thefollowing code snippet:

```
또한 인덱싱, 분할, 추가, 팝핑 등의 다양한 작업을 목록에서 수행 할 수 있습니다. 목록의 일부 일반적인 작업은 다음 코드 스 니펫에 나와 있습니다.
```



```python
In [167]: # indexing lists
In [168]: l1
Out[168]: ['eggs', 'flour', 'butter']
In [169]: l1[0]
Out[169]: 'eggs'
In [170]: l1[1]
Out[170]: 'flour'
In [171]: l1[0] +' '+ l1[1]
Out[171]: 'eggs flour'
In [171]: # slicing lists
In [172]: l2[1:3]
Out[172]: ['drink', 10]
In [173]: numbers = range(10)
In [174]: numbers
Out[174]: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
In [175]: numbers[2:5]
Out[175]: [2, 3, 4]
In [180]: numbers[:]
Out[180]: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
In [181]: numbers[::2]
Out[181]: [0, 2, 4, 6, 8]
In [181]: # concatenating and mutating lists
In [182]: numbers * 2
Out[182]: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
In [183]: numbers + l2
Out[183]: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 1, 'drink', 10, 'sandwiches',0.0045]
In [184]: # handling nested lists
In [184]: l3
Out[184]: [1, 2, 3, ['a', 'b', 'c'], ['Hello', 'Python']]
In [185]: l3[3]
Out[185]: ['a', 'b', 'c']
In [186]: l3[4]
Out[186]: ['Hello', 'Python']
In [187]: l3.append(' '.join(l3[4]))  # append operation
In [188]: l3
Out[188]: [1, 2, 3, ['a', 'b', 'c'], ['Hello', 'Python'], 'Hello Python']
In [189]: l3.pop(3)  # pop operation
Out[189]: ['a', 'b', 'c']
In [190]: l3
Out[190]: [1, 2, 3, ['Hello', 'Python'], 'Hello Python']
```

### Sets

Sets are unordered collections of unique and immutable objects. You can use the set()function or the curly braces {...} to create a new set. Sets are typically used to removeduplicates from a list, test memberships, and perform mathematical set operations,including union, intersection, difference, and symmetric difference.

Some set representations and operations are shown in the following code snippet:

```
세트는 일그러지고 변경되지 않는 객체의 순서가 없는 콜렉션입니다. set () 함수 또는 중괄호 ({})를 사용하여 새 세트를 만들 수 있습니다. 

집합은 일반적으로 목록에서 중복을 제거하고 멤버십을 테스트하고 조합, 교차점, 차이점 및 대칭 차이를 비롯한 수학적 집합 연산을 수행하는 데 사용됩니다.

일부 세트 표현과 조작은 다음 코드 스 니펫에 표시됩니다.
```

```
In [196]: l1 = [1,1,2,3,5,5,7,9,1]
```

```
In [197]: set(l1)  # makes the list as a set
Out[197]: {1, 2, 3, 5, 7, 9}
```

74

```
In [198]: s1 = set(l1)
```

```
# membership testing
In [199]: 1 in s1
Out[199]: True
In [200]: 100 in s1
Out[200]: False
```

```
# initialize a second set
In [201]: s2 = {5, 7, 11}
```

```
# testing various set operations
In [202]: s1 - s2  # set difference
Out[202]: {1, 2, 3, 9}
```

```
In [203]: s1 | s2  # set union
Out[203]: {1, 2, 3, 5, 7, 9, 11}
```

```
In [204]: s1 & s2  # set intersection
Out[204]: {5, 7}
```

```
In [205]: s1 ^ s2  # elements which do not appear in both sets
Out[205]: {1, 2, 3, 9, 11}
```

### Dictionaries

Dictionaries in Python are key-value mappings that are unordered and mutable. They
are often known as hashmaps, associative arrays, and associative memories. Dictionaries
are indexed using keys, which can be any immutable object type, like numeric types or
strings, or even tuples, which we will see later on. Remember that keys should always
be some immutable data type. Dictionary values can be immutable or mutable objects,
including lists and dictionaries themselves which would lead to nested dictionaries.
Dictionaries have a lot of similarity with JSON objects, if you have worked with them
previously. Dictionaries are often called dicts in Python, and the dict() function is also
used to create new dictionaries.

The following code snippets show some representations and operations ondictionaries:

```
파이썬의 사전은 정렬되지 않고 변경 가능한 키 - 값 매핑입니다. 이들은 종종 해시 맵, 연관 배열 및 연관 메모리로 알려져 있습니다. 사전은 키를 사용하여 색인화됩니다.이 키는 숫자 유형이나 문자열 또는 심지어 튜플과 같은 불변 개체 유형 일 수 있습니다. 나중에 튜토리얼을 보겠습니다. 키는 항상 변경 불가능한 데이터 유형이어야합니다. 사전 값은 중첩 된 사전으로 이어질 목록 및 사전 자체를 포함하여 변경 불가능하거나 변경 가능한 개체 일 수 있습니다. 사전은 이전에 JSON 객체와 작업 한 적이 있다면 JSON 객체와 많이 유사합니다. 사전은 종종 Python에서 dicts라고하며 dict () 함수는 새 사전을 만드는데도 사용됩니다. 

다음 코드 스니 j에서는 사전에 표현과 조작을 보여줍니다.
```

```
In [207]: d1 = {'eggs': 2, 'milk': 3, 'spam': 10, 'ham': 15}
In [208]: d1
Out[208]: {'eggs': 2, 'ham': 15, 'milk': 3, 'spam': 10}
```

```
# retrieving items based on key
In [209]: d1.get('eggs')
Out[209]: 2
In [210]: d1['eggs']
Out[210]: 2
```

```
# get is better than direct indexing since it does not throw errors
In [211]: d1.get('orange')
In [212]: d1['orange']
Traceback (most recent call last):
  File "<ipython-input-212-ebecbf415243>", line 1, in <module>
    d1['orange']
    KeyError: 'orange'
```

```
# setting items with a specific key
In [213]: d1['orange'] = 25
In [214]: d1
Out[214]: {'eggs': 2, 'ham': 15, 'milk': 3, 'orange': 25, 'spam': 10}
```

```
# viewing keys and values
In [215]: d1.keys()
Out[215]: ['orange', 'eggs', 'ham', 'milk', 'spam']
In [216]: d1.values()
Out[216]: [25, 2, 15, 3, 10]
```

```
# create a new dictionary using dict function
In [219]: d2 = dict({'orange': 5, 'melon': 17, 'milk': 10})
In [220]: d2
Out[220]: {'melon': 17, 'milk': 10, 'orange': 5}
```

```
# update dictionary d1 based on new key-values in d2
In [221]: d1.update(d2)
In [222]: d1
Out[222]: {'eggs': 2, 'ham': 15, 'melon': 17, 'milk': 10, 'orange': 5,'spam': 10}
```

```
# complex and nested dictionary
In [223]: d3 = {'k1': 5, 'k2': [1,2,3,4,5], 'k3': {'a': 1, 'b': 2, 'c':[1,2,3]}}
In [225]: d3
Out[225]: {'k1': 5, 'k2': [1, 2, 3, 4, 5], 'k3': {'a': 1, 'b': 2, 'c': [1, 2, 3]}}
In [226]: d3.get('k3')
Out[226]: {'a': 1, 'b': 2, 'c': [1, 2, 3]}
In [227]: d3.get('k3').get('c')
Out[227]: [1, 2, 3]
```

### Tuples

Tuples are also sequences like lists, but they are immutable. Typically, tuples are usedto represent fixed collections of objects or values. Tuples are created using a comma-separated sequence of values enclosed by parentheses, and optionally the tuple()function can also be used.

The following code snippet shows some representations and operations on tuples:

```
튜플은 목록과 같은 시퀀스이지만 불변입니다. 
일반적으로 튜플은 객체 또는 값의 고정 된 컬렉션을 나타 내기위해 사용됩니다. 
튜플은 괄호로 묶인 쉼표로 구분 된 값의 시퀀스를 사용하여 작성되며 선택적으로 tuple () 함수를 사용할 수도 있습니다.

다음 코드 스 니펫은 튜플에 대한 표현과 연산을 보여줍니다.
```

```
# creating a tuple with a single element
In [234]: single_tuple = (1,)
In [235]: single_tuple
Out[235]: (1,)

```

```
# original address of the tuple
In [239]: id(single_tuple)
Out[239]: 176216328L
```

```
# modifying contents of the tuple but its location changes (new tuple is
created)
In [240]: single_tuple = single_tuple + (2, 3, 4, 5)
In [241]: single_tuple
Out[241]: (1, 2, 3, 4, 5)
In [242]: id(single_tuple) # different address indicating new tuple with same name
Out[242]: 201211312L
```

```
# tuples are immutable hence assignment is not supported like lists
In [243]: single_tuple[3] = 100
Traceback (most recent call last):
  File "<ipython-input-247-37d1946d4128>", line 1, in <module>

single_tuple[3] = 100
TypeError: 'tuple' object does not support item assignment
```

```
# accessing and unpacking tuples
In [243]: tup = (['this', 'is', 'list', '1'], ['this', 'is', 'list', '2'])
In [244]: tup[0]
Out[244]: ['this', 'is', 'list', '1']
In [245]: l1, l2 = tup
In [246]: print l1, l2
['this', 'is', 'list', '1'] ['this', 'is', 'list', '2']
```

### Files

Files are special types of objects in Python that are used mainly for interfacing withexternal objects in the filesystem, including text, binary, audio, and video files, plusdocuments, images, and many more. Some might disagree about it being a data type inPython, but it actually is a special data type, and the name of the type, file, suits its roleperfectly for handling all types of external files. You usually use the open() function toopen a file, and there are various modes like read and write that are specified using aprocessing mode character in the function.

Some examples of file handling are show in the following code snippet:

```
파일은 파이썬에서 텍스트, 바이너리, 오디오 및 비디오 파일, 플러스 문서, 이미지 등을 포함하여 파일 시스템의 외부 객체를 인터페이싱하는 데 주로 사용되는 특수한 유형의 객체입니다. 

일부는 inPython의 데이터 유형이라는 점에 동의하지 않지만 실제로는 특수한 데이터 유형이며 유형의 파일 이름은 모든 유형의 외부 파일을 처리하기 위해 해당 역할에 적합합니다. 

일반적으로 open () 함수를 사용하여 파일을 열고, 함수에서 처리 모드 문자를 사용하여 지정된 읽기 및 쓰기와 같은 다양한 모드가 있습니다.

파일 처리의 몇 가지 예는 다음 코드 스 니펫에 표시됩니다.
```



```
In [253]: f = open('text_file.txt', 'w')   # open in write mode
In [254]: f.write("This is some text\n")  # write some text
In [255]: f.write("Hello world!")
In [256]: f.close()  # closes the file
```

```
# lists files in current directory
In [260]: import os
In [262]: os.listdir(os.getcwd())
Out[262]: ['text_file.txt']
```

```
In [263]: f = open('text_file.txt', 'r')  # opens file in read mode
In [264]: data = f.readlines()  # reads in all lines from file
In [265]: print data  # prints the text data
['This is some text\n', 'Hello world!']
```

### Miscellaneous

Besides the already mentioned data types and structures, there are several other Pythondata types:

- The None type indicates no value/no data or null object.

- Boolean types include True and False.

- Decimal and Fraction types handle numbers in a better way.

  This completes the list for Python’s core data types and data structures that you willbe using most of the time in your code and implementations. We will now discuss someconstructs typically used for controlling the flow of code.


```
이미 언급 한 데이터 유형과 구조 외에도 여러 다른 Pythondata 유형이 있습니다.

- 없음 유형은 값 / 데이터 없음 또는 널 (NULL) 오브젝트를 표시하지 않습니다.
- 부울 유형에는 True 및 False가 포함됩니다. Decimal 및 Fraction 유형은 숫자를보다 잘 처리합니다.
- 이렇게하면 Python의 핵심 데이터 유형과 코드 및 구현에서 대부분의 시간을 사용할 데이터 구조에 대한 목록이 완성됩니다. 이제는 코드의 흐름을 제어하는 데 일반적으로 사용되는 someconstructs에 대해 논의 할 것입니다.
```



## Controlling Code Flow

Flow of code is extremely important. A lot of it is based on business logic and rules. It alsodepends on the type of implementation decisions developers take when building systemsand applications. Python provides several control flow tools and utilities that can be usedto control the flow of your code. Here are the most popular ones:

- if-elif-else conditionals

- for loop

- while loop

- break, continue, and else in loops

- try-except

These constructs will help you understand several concepts including conditionalcode flow, looping, and handling exceptions.

```
코드의 흐름은 매우 중요합니다. 많은 것은 비즈니스 논리와 규칙을 기반으로합니다. 개발자는 시스템 및 응용 프로그램을 작성할 때 개발자가 취하는 결정의 유형을 결정합니다. Python은 코드의 흐름을 제어하는 데 사용할 수있는 몇 가지 제어 흐름 도구와 유틸리티를 제공합니다. 다음은 가장 인기있는 것들입니다 :

- if-elif-else conditionals
- for loop
- while loop
- break, continue, and else in loops
- try-except


이러한 구조는 조건부 코드 흐름, 루핑 및 예외 처리를 비롯한 여러 개념을 이해하는 데 도움이됩니다.
```



###Conditional Constructs

The concept of conditional code flow involves executing different blocks of code
conditionally based on some user-defined logic implemented in the code itself. It is
extremely useful when you do not want to execute a block of statements sequentially
one after the other but execute a part of them based on fulfilling or not fulfilling certain
conditions. The if-elif-else statements help in achieving this. The general syntax for it is as
follows:

```
- 조건부 코드 흐름의 개념은 코드 자체에 구현 된 일부 사용자 정의 논리를 기반으로 조건부로 다른 코드 블록을 실행하는 것을 포함합니다. 

- 한 문장 씩 순차적으로 문장을 실행하고 싶지는 않지만 특정 조건을 충족 시키거나 충족시키지 않는 것을 기준으로 문장의 일부를 실행하려는 경우 매우 유용합니다. 

- if-elif-else 문은 이를 달성하는 데 도움이됩니다. 일반적인 구문은 다음과 같습니다.
```

```
if <conditional check 1 is True>:    # the if conditional (mandatory)
    <code block 1>   # executed only when check 1 evaluates to True
        ...
    <code block 1>
elif <conditional check 2 is True>:  # the elif conditional (optional)
    <code block 2>
        ...
    <code block 2>
else:
    <code block 3>
        ...
    <code block 3>
# executed only when check 1 is False and 2 is True
# the else conditional (optional)
# executed only when check 1 and 2 are False
```

An important point to remember from the preceding syntax is that the correspondingcode blocks only execute based on satisfying the necessary conditions. Also, only the ifstatement is mandatory, and the elif and else statements do not need to be mentionedunless there is a need based on conditional logic.

The following examples depict conditional code flow:

```
앞의 구문에서 기억해야 할 중요한 점은 해당 코드 블록이 필요한 조건을 만족하는 경우에만 실행된다는 것입니다. 또한 ifstatement 만 필수이며 elif 및 else 문은 조건부 논리를 기반으로 필요가 없다면 언급 할 필요가 없습니다.

다음 예제는 조건부 코드 흐름을 보여줍니다.
```

```
In [270]: var = 'spam'
In [271]: if var == 'spam':
     ...:     print 'Spam'
	 ...:Spam
In [272]: var = 'ham'
In [273]: if var == 'spam':
     ...:     print 'Spam'
     ...: elif var == 'ham':
     ...:     print 'Ham'
     ...:Ham
 
In [274]: var = 'foo'
In [275]: if var == 'spam':
     ...:     print 'Spam'
     ...: elif var == 'ham':
     ...:     print 'Ham'
     ...: else:
     ...:     print 'Neither Spam or Ham'
     ...:
Neither Spam or Ham
```

### Looping Constructs

There are two main types of loops in Python: for and while loops. These loopingconstructs are used to execute blocks of code repeatedly until some condition is satisfiedor the loop exits based on some other statements or conditionals.

The for statement is generally used to loop through items in sequence and usually
loops through one or many iterables sequentially, executing the same block of code in
each turn. The while statement is used more as a conditional general loop, which stops
the loop once some condition is satisfied or runs the loop till some condition is satisfied.
Interestingly, there is an optional else statement at the end of the loops that is executed
only if the loop exits normally without any break statements. The break statement is often
used with a conditional to stop executing all statements in the loop immediately and exit the
closest enclosing loop. The continue statement stops executing all statements below it in
the loop and brings back control to the beginning of the loop for the next iteration. The pass
statement is just used as an empty placeholder—it does not do anything and is often used to
indicate an empty code block. These statements constitute the core looping constructs.

The following snippets show the typical syntax normally used when constructing forand while loops:

```
파이썬에는 두 가지 주요 유형의 루프가 있습니다 : for 및 while 루프. 
이러한 루프 구성은 일부 조건이 충족되거나 루프가 일부 다른 명령문이나 조건에 따라 종료 될 때까지 반복적으로 코드 블록을 실행하는 데 사용됩니다.

for 문은 일반적으로 순차적으로 항목을 반복하는 데 사용되며 대개 순차적으로 하나 또는 여러 개의 반복 가능한 반복을 통해 동일한 코드 블록을 실행합니다. 

while 문은 조건부 일반 루프로 더 많이 사용되며, 일부 조건이 만족되면 루프를 중지하거나 일부 조건이 충족 될 때까지 루프를 실행합니다.

흥미롭게도 루프의 끝 부분에 선택적 else 문이 있습니다.이 문은 루프가 break 문 없이 정상적으로 종료되는 경우에만 실행됩니다. 
break 문은 종종 조건부와 함께 사용되어 루프의 모든 문을 즉시 실행을 중지하고 가장 가까운 폐 루프를 종료합니다. 

continue 문은 루프에서 그 아래에 있는 모든 문을 실행을 중지하고 다음 반복을 위해 루프의 시작 부분으로 제어를 되돌립니다. 

pass 문은 빈 자리 표시자로 사용되며 아무것도 수행하지 않고 빈 코드 블록을 나타내는 데 자주 사용됩니다. 이 문장은 핵심 루핑 구조를 구성합니다.

다음 스 니펫은 forand while 루프를 생성 할 때 일반적으로 사용되는 일반적인 구문을 보여줍니다.
```



```
# the for loop
for item in iterable:  # loop through each item in the iterable
    <code block>
else:


<code block>

# Code block executed repeatedly
   # Optional else

# code block executes only if loop exits normally
without 'break'

# the while loop
while <condition>:  # loop till condition is satisfied

    <code block>
else:

<code block>

# Code block executed repeatedly
   # Optional else

# code block executes only if loop exits normally
without 'break'
```

The following examples show how loops work along with the other loopingconstructs including pass, break, and continue:

```
# illustrating for loops
In [280]: numbers = range(0,5)
In [281]: for number in numbers:

     ...:     print number
     ...:

0
1
2
3
4
In [282]: sum = 0
In [283]: for number in numbers:
     ...:     sum += number
     ...:
In [284]: print sum

# role of the trailing else and break constructs
In [285]: for number in numbers:
     ...:     print number
     ...: else:
     ...:     print 'loop exited normally'
     ...:
0
1
2
3
4
loop exited normally
In [286]: for number in numbers:
     ...:
     ...:
     ...:
     ...:
     ...: else:
     ...:     print 'loop exited normally'
     ...:
# illustrating while loops
In [290]: number = 5
In [291]: while number > 0:
       ...:      print number
       ...:      number -= 1  # important! else loop will keep running
       ...:
  54321
if number < 3:
    print number
else:break

# role of continue construct
In [295]: number = 10
In [296]: while number > 0:
     ...:
     ...:
     ...:
iteration
     ...:
     ...:
     ...:
108642

if number % 2 != 0:
    number -=1 # decrement but do not print odd numbers
    continue  # go back to beginning of loop for next
print number  # print even numbers and decrement count
number -= 1

# role of the pass construct
In [297]: number = 10
In [298]: while number > 0:
     ...:
     ...:
     ...:
     ...:
     ...:
     ...:
108642

if number % 2 != 0:
    pass # don't print odds
else:
    print number

number -= 1
```

### Handling Exceptions

Exceptions are specific events that are either triggered when some unnatural error
occurs or manually. They are used extensively for error handling, event notifications, and
controlling code flow. Using constructs like try-except-finally, you can make Python
raise exceptions when executing code whenever any error occurs at runtime. This would
also enable you to catch these exceptions and handle them as needed or ignore them
altogether. In Python versions prior to 2.5.x, there were generally two versions of exception
handling using the try construct. One would be try-finally, and the other would involve
try-except and optionally an else clause at the end for catching exceptions. Now we have
a construct that includes them all, the try-except-else-finally construct, which can be
used for exception handling. The syntax is depicted as follows:

```
예외는 부 자연스러운 오류가 발생할 때 또는 수동으로 트리거되는 특정 이벤트입니다. 오류 처리, 이벤트 알림 및 제어 코드 흐름을 위해 광범위하게 사용됩니다. try-except-finally와 같은 구문을 사용하면 런타임에 오류가 발생할 때마다 코드를 실행할 때 Python에서 예외를 발생시킬 수 있습니다. 또한 이러한 예외를 포착하여 필요에 따라 처리하거나 모두 무시할 수 있습니다. 2.5.x 이전의 Python 버전에는 일반적으로 try 구조를 사용하는 두 가지 버전의 예외 처리가있었습니다. 하나는 try-finally이고, 다른 하나는 try-except와 예외적으로 예외를 잡는 끝에 else 절을 포함합니다. 이제는 예외 처리를 위해 사용할 수있는 try-except-else-finally 구문을 모두 포함하는 구조를 만들었습니다. 구문은 다음과 같이 표시됩니다.
```

```
try:
    <main code block>

```

```
except <ExceptionType1>:

```

```
     # The try statement
# Checks for errors in this block

```

```
     # Catch different exceptions

```

82

```
    <exception handler 1>
except <ExceptionType2>:

```

```
    <exception handler 2>
...

```

```
else:
    <optional else block>  # Executes only if there were no exceptions

```

```
finally:                        # The finally statement
    <finally block>        # Always executes in the end

```

The flow of code in the preceding code snippet starts from the try statement and
themain code blockinit,whichisexecutedfirstandcheckedforanyexceptions.If
any exceptions occur, they are matched based on the exception types as depicted in
the preceding snippet. Assuming ExceptionType1 matches, the exception handler for
ExceptionType1 is executed, which is exception handler 1. In case no exceptions were
raised,onlythentheoptional else blockisexecuted.Thefinally blockisalways
executed irrespective of any exceptions being raised or not.

The following examples depict the use of the try-except-else-finally construct:

```
앞의 코드 조각에서 코드 흐름은 try 문과 주 코드 블록에서 시작됩니다.이 코드 블록은 예외에 대해 먼저 실행되고 검사됩니다. 예외가 발생하면 앞의 조각에서 설명한대로 예외 유형에 따라 일치합니다. ExceptionType1이 일치하면 예외 핸들러 1 인 ExceptionType1에 대한 예외 핸들러가 실행됩니다. 예외가 발생하지 않은 경우에만 다른 옵션 블록이 실행됩니다. 예외적으로 예외 발생 여부와 관계없이 최종 블록은 항상 실행됩니다.

다음 예제는 try-except-else-finally 구문을 사용하는 방법을 보여줍니다.
```



```
In [311]: shopping_list = ['eggs', 'ham', 'bacon']
# trying to access a non-existent item in the list
In [312]: try:

```

```
     ...:     print shopping_list[3]
     ...: except IndexError as e:
     ...:     print 'Exception: '+str(e)+' has occurred'
     ...: else:
     ...:     print 'No exceptions occurred'
     ...: finally:
     ...:     print 'I will always execute no matter what!'
     ...:

```

```
Exception: list index out of range has occurred
I will always execute no matter what!
# smooth code execution without any errors
In [313]: try:

```

```
     ...:     print shopping_list[2]
     ...: except IndexError as e:
     ...:     print 'Exception: '+str(e)+' has occurred'
     ...: else:
     ...:     print 'No exceptions occurred'
     ...: finally:
     ...:     print 'I will always execute no matter what!'
     ...:

```

```
bacon
No exceptions occurred
I will always execute no matter what!

```

This brings us to the end of our discussion on the core constructs for controlling flowof code in Python. The next section covers some core concepts and constructs that areparts of the functional programming paradigm in Python.

```
이것은 파이썬에서 플로우 우드 코드를 제어하기위한 핵심 구조에 대한 논의를 끝내게합니다. 다음 섹션은 파이썬에서 기능 프로그래밍 패러다임의 일부 핵심 개념과 구성을 다루고 있습니다.
```



```
# Optional else statement
```

##Functional Programming

The functional programming paradigm is a style of programming with origins in lambdacalculus. It treats any form of computation purely on the basis of executing and evaluatingfunctions. Python is not a pure functional programming language but does have severalconstructs that can be used for functional programming. In this section we will talk

about several of these constructs, including functions and some advanced concepts likegenerators, iterators, and comprehensions. We will also look at modules like itertoolsand functools that contain implementation of functional tools based on concepts fromHaskell and Standard ML.

```
기능적 프로그래밍 패러다임은 lambdacalculus에서 시작된 프로그래밍 스타일입니다. 이것은 실행 및 평가 기능을 기준으로 모든 형태의 계산을 처리합니다. 파이썬은 순수한 함수형 프로그래밍 언어는 아니지만 함수형 프로그래밍에 사용될 수있는 몇 가지 구조를 가지고 있습니다. 

이 섹션에서는 생성자, 반복자, 이해력과 같은 몇 가지 고급 개념과 함수를 비롯한 몇 가지 구문에 대해 설명합니다. 또한 Haskell과 Standard ML의 개념을 기반으로 한 기능적 툴의 구현을 포함하는 itertools와 functools 같은 모듈을 살펴볼 것이다.
```



###Functions

A function can be defined as a block of code that is executed only on request by invokingit. Functions consist of a function definition that has the function signature (functionname, parameters) and a group of statements inside the function that are executed whenthe function is called. The Python standard library provides a huge suite of functions tochoose from to perform different types of operations. Besides this, users can define theirown functions using the def keyword.

Functions usually return some value always, and even when they do not return avalue, by default they return the None type. One important thing to remember is that oftenyou may see methods and functions being used interchangeably, but the distinctionbetween functions and methods is that methods are functions that are defined withinclass statements. Functions are also objects, since each and every type and construct inPython is derived from the base object type. This opens up a whole new dimension whereyou can even pass functions as parameters or arguments to other functions. Moreover,functions can be bound to variables and even returned as results from other functions.Hence functions are often known as first-class objects in Python.

The following code snippet shows the basic structure of a function definition inPython:

```
함수는 invokingit에 의해 요청시에만 실행되는 코드 블록으로 정의 될 수 있습니다. 함수는 함수 서명 (functionname, parameters) 및 함수가 호출 될 때 실행되는 함수 내부의 명령문 그룹을 갖는 함수 정의로 구성됩니다. Python 표준 라이브러리는 다양한 유형의 작업을 수행 할 수있는 기능을 제공합니다. 이 외에도 사용자는 def 키워드를 사용하여 확장 함수를 정의 할 수 있습니다.

함수는 대개 항상 값을 반환하며, 값이 반환되지 않는 경우에도 기본적으로 없음 유형을 반환합니다. 기억해야 할 중요한 사실은 메소드와 함수가 서로 교환되어 사용되는 것을 종종 볼 수 있지만 함수와 메소드의 구분은 메소드가 클래스 문에서 정의 된 함수라는 점입니다. 함수는 또한 객체이기 때문에 inPython의 모든 유형과 구조는 기본 객체 유형에서 파생되기 때문에 함수입니다. 이렇게하면 함수를 매개 변수 나 인수로 다른 함수에 전달할 수있는 완전히 새로운 차원이 열립니다. 또한, 함수는 변수에 바인딩 될 수 있으며 심지어 다른 함수의 결과로 반환 될 수도 있습니다 .Hence 함수는 종종 Python에서 일류 객체로 알려져 있습니다.

다음 코드 스니 j은 함수 정의 inPython의 기본 구조를 보여줍니다.
```



```
def function(params):  # params are the input parameters
    <code block>       # code block consists of a group of statements
    return value(s)    # optional return statement

```

The params indicate the list of input parameters, which are not mandatory, and inmany functions there are actually no input parameters. You can even pass functionsthemselves as parameters. Some logic executes in the code block, which may or may notmodify the input parameters, and finally you may return some output values or not returnanything entirely.

The following code snippets demonstrate some basic examples of functions withfixed arguments, variable arguments, and built-in functions:

```
매개 변수는 입력 매개 변수 목록을 나타내며 필수 매개 변수는 아니며 실제로는 입력 매개 변수가 없습니다. 당신은 매개 변수로서 스스로 기능을 전달할 수도 있습니다. 일부 로직은 코드 블록에서 실행되며 입력 매개 변수를 수정하거나 수정하지 않을 수도 있습니다. 마지막으로 일부 출력 값을 반환하거나 반환하지 않을 수도 있습니다.

다음 코드 스니 j은 고정 인수, 가변 인수 및 내장 함수가있는 함수의 몇 가지 기본 예를 보여줍니다.
```



```
# function with single argument
In [319]: def square(number):

```

```
     ...:     return number*number
     ...:

```

84

```
In [320]: square(5)
Out[320]: 25

```

```
# built-in function from the numpy library
In [321]: import numpy as np
In [322]: np.square(5)
Out[322]: 25

```

```
# a more complex function with variable number of arguments
In [323]: def squares(*args):

```

- ```
       ...:      squared_args = []
   ```

  ```

- ```
       ...:      for item in args:

  ```

- ```
       ...:          squared_args.append(item*item)
   ```

  ```

- ```
       ...:      return squared_args
       ...:

  ```

  ```
  In [324]: squares(1,2,3,4,5)
  Out[324]: [1, 4, 9, 16, 25]

  ```

  The preceding example shows how to introduce variable number of arguments in afunction dynamically. You can also introduce keyword arguments, where each argumenthas its own variable name and value, as illustrated in the following code snippet:

```
앞의 예는 함수에 동적으로 인수의 수를 가변적으로 도입하는 방법을 보여줍니다. 다음 코드 스 니펫 에서처럼 키워드 인수를 도입 할 수도 있습니다. 각 인수는 자체 변수 이름과 값을 갖습니다.
```

  ```
  # assign specific keyword based arguments dynamically
  In [325]: def person_details(**kwargs):

  ```

  ```
       ...:     for key, value in kwargs.items():
       ...:         print key, '->', value
       ...:

  ```

  ```
  In [326]: person_details(name='James Bond', alias='007', job='Secret Service
            Agent')

  ```

  ```
  alias -> 007
  job -> Secret Service Agent
  name -> James Bond

  ```

###Recursive Functions

  Recursive functions use the concept of recursion, wherein the function calls itself insideits code block. Care should be taken to make sure there is a stopping condition thatultimately terminates the recursive calls—otherwise the function will run into an endlessloop of execution where it goes on calling itself. Recursion makes use of the call stack ateach recursive call, hence they are often not very efficient compared to regular functions;nevertheless, they are extremely powerful.

  The following example depicts our squares function using recursion:

```
재귀 함수는 재귀라는 개념을 사용하는데,이 함수는 코드 블록 내에서 코드 블록을 호출합니다. 재귀 호출을 종료하는 중지 조건이 있는지 확인하는 데주의해야합니다. 그렇지 않으면 함수 자체가 호출 될 때 끝없이 실행됩니다. 재귀 호출마다 재귀 호출을 사용하므로 정규 함수와 비교할 때 효율성이 떨어지는 경우가 많지만 극도로 강력합니다.

   다음 예제는 재귀를 사용하여 square 함수를 보여줍니다.
```



  ```
  # using recursion to square numbers
  In [331]: def recursive_squares(numbers):

  ```

  ```
       ...:     if not numbers:
       ...:         return []
  ```

```
     ...:     else:
     ...:         return [numbers[0]*numbers[0]] + recursive_

```

```
                  squares(numbers[1:])

```

```
     ...:
In [332]: recursive_squares([1, 2, 3, 4, 5])
Out[332]: [1, 4, 9, 16, 25]

```

###Anonymous Functions

Anonymous functions are functions that do not have any name and usually consist of
a one-line expression that denotes a function using the lambda construct. The lambda
keyword is used to define inline function objects that can be used just like regular
functions, with a few differences. The general syntax for a lambda function is shown in the
following code snippet:

```
익명 함수는 이름이 없으며 대개 람다 구문을 사용하는 함수를 나타내는 한 줄 표현식으로 구성되는 함수입니다. lambda 키워드는 몇 가지 차이점을 제외하고 일반 함수처럼 사용할 수있는 인라인 함수 객체를 정의하는 데 사용됩니다. 람다 함수의 일반 구문은 다음 코드 스 니펫에 나와 있습니다.
```



```
lambda arg, arg2,... arg_n : <inline expression using args>

```

This expression can actually be even assigned to variables and then executed as anormal function call similar to functions created with def. However, lambda functions areexpressions and never statements like the code block inside a def, and so it is extremelydifficult to put complex logic inside a lambda function because it is always a single-linedinline expression. However, lambda functions are very powerful and are even used insidelists, functions, and function arguments. Besides lambda functions, Python also providesfunctions like map(), reduce(), and filter(), which make extensive use of lambdafunctions and apply them to iterables usually to transform, reduce, or filter respectively.

The following code snippet depicts some examples of lambda functions used with theconstructs we just talked about:

```
이 표현식은 실제로 변수에 할당 된 다음 def로 작성된 함수와 유사한 비정규 함수 호출로 실행될 수도 있습니다. 그러나 람다 함수는 def 내부의 코드 블록과 같은 표현식과 never 문이므로 항상 람다 함수 내에 복잡한 논리를 넣는 것은 매우 어렵습니다. 이는 항상 단일 라인 식이기 때문에입니다. 그러나 람다 함수는 매우 강력하며 insidelists, 함수, 함수 인자로도 사용됩니다. 람다 함수 외에도, 파이썬은 lambdafunction을 광범위하게 사용하고이를 변환, 축소 또는 필터링하기위한 iterable에 일반적으로 적용하는 map (), reduce () 및 filter ()와 같은 함수를 제공합니다.

다음 코드 스 니펫은 방금 이야기 한 구성과 함께 사용되는 람다 함수의 몇 가지 예를 보여줍니다.
```



```
# simple lambda function to square a number
In [340]: lambda_square = lambda n: n*n
In [341]: lambda_square(5)
Out[341]: 25

```

```
# map function to square numbers using lambda
In [342]: map(lambda_square, [1, 2, 3, 4, 5])
Out[342]: [1, 4, 9, 16, 25]

```

```
# lambda function to find even numbers used for filtering
In [343]: lambda_evens = lambda n: n%2 == 0
In [344]: filter(lambda_evens, [1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
Out[344]: [2, 4, 6, 8, 10]

```

```
# lambda function to add numbers used for adding numbers in reduce function
In [345]: lambda_sum = lambda x, y: x + y
In [346]: reduce(lambda_sum, [1, 2, 3, 4, 5])
Out[346]: 15

```

86

```
# lambda function to make a sentence from word tokens with reduce function
In [347]: lambda_sentence_maker = lambda word1, word2: ' '.join([word1,

```

```
          word2])
In [348]: reduce(lambda_sentence_maker, ['I', 'am', 'making', 'a',

```

```
          'sentence', 'from', 'words!'])
Out[348]: 'I am making a sentence from words!'

```

The preceding examples should give you a pretty good idea about how lambdafunctions work and how powerful they are. Using a one-line construct you can createfree-flowing sentences from word tokens and calculate a sum of numbers in a list! Thepossibilities of using lambda functions are endless, and you can use them to solve eventhe most complex of problems.

```
위의 예제는 람다 함수가 어떻게 작동하고 얼마나 강력한 지에 대한 좋은 아이디어를 제공합니다. 한 줄짜리 구문을 사용하여 단어 토큰에서 자유롭게 흐르는 문장을 만들고 목록에있는 숫자의 합을 계산할 수 있습니다! 람다 함수 사용의 가능성은 무한하며, 가장 복잡한 문제를 해결할 수 있습니다.
```



###Iterators

Iterators are constructs used to iterate through iterables. Iterables are objects that are
basically sequences of other objects and data. A good example would be a for loop, which is
actually an iterable that iterates through a list or sequence. Iterators are objects or constructs
that can be used to iterate through iterables using the next()function, which returns the next
item from the iterable at each call. Once it has iterated through the entire iterable, it returns
a StopIteration exception. We have seen how a for loop works in general, however behind
the abstraction, the for loop actually calls the iter() function on the iterable to create an
iterator object and then traverses through it using the next() function.

The following example illustrates how iterators work:

```
반복자는 반복 가능을 통해 반복하는 데 사용되는 구문입니다. 반복문은 기본적으로 다른 객체와 데이터의 시퀀스 인 객체입니다. 좋은 예제는 for 루프입니다. 실제로는 반복문이나 시퀀스를 반복하는 iterable입니다. 반복자는 각 호출시 iterable에서 다음 항목을 반환하는 next () 함수를 사용하여 iterables를 반복하는 데 사용할 수있는 객체 또는 구문입니다. 전체 iterable을 반복하면 StopIteration 예외가 반환됩니다. 우리는 for 루프가 일반적으로 어떻게 작동 하는지를 보았지만, 추상화 뒤에서 for 루프는 실제로 iterable 객체를 생성하기 위해 iter () 함수를 호출하고 next () 함수를 사용하여 iterator 객체를 가로 지른다.
다음 예제에서는 반복기의 작동 방식을 보여줍니다.
```



```
# typical for loop
In [350]: numbers = range(6)
In [351]: for number in numbers:

```

```
     ...:     print number
0

```

12345

```
# illustrating how iterators work behind the scenes
In [352]: iterator_obj = iter(numbers)
In [353]: while True:

```

012

```
...:
...:
...:
...:
...:

```

```
try:
    print iterator_obj.next()

```

```
except StopIteration:
    print 'Reached end of sequence'
    break
```

```
3
4
5
Reached end of sequence

```

```
# calling next now would throw the StopIteration exception as expected
In [354]: iterator_obj.next()
Traceback (most recent call last):

```

```
  File "<ipython-input-354-491178c4f97a>", line 1, in <module>
    iterator_obj.next()

```

```
StopIteration

```

###Comprehensions

Comprehensions are interesting constructs that are similar to for loops but moreefficient. They fall rightly into the functional programming paradigm following the setbuilder notation. Originally, the idea for list comprehensions came from Haskell, andafter a series of lengthy discussions comprehensions were finally added and have beenone of the most used constructs ever since. There are various types of comprehensionsthat can be applied on existing data types, including list, set, and dict comprehensions.The following code snippet shows the syntax of comprehensions using the very commonlist comprehensions and for loops, a core component in comprehensions:

```
이해는 for 루프와 유사하지만보다 효율적인 흥미로운 구성입니다. 그들은 setbuilder 표기법에 따라 기능 프로그래밍 패러다임에 빠지게됩니다. 원래 목록 내포에 대한 아이디어는 하스켈에서 나온 것이었고, 이후에 일련의 긴 토론의 이해가 마침내 추가되어 그 이후로 가장 많이 사용 된 구조로 남게되었습니다. list, set, dict comprehension을 포함하여 기존 데이터 유형에 적용 할 수있는 다양한 유형의 이해가 있습니다. 다음 코드 스 니펫은 comprehensions의 핵심 구성 요소 인 매우 공통 목록 comprehension 및 for 루프를 사용하여 comprehension의 구문을 보여줍니다.
```

```
# typical comprehension syntax
[ expression for item in iterable ]

```

```
# equivalent for loop statement
for item in iterable:

```

expression

```
# complex and nested iterations
[ expression for item1 in iterable1 if condition1

```

```
             for item2 in iterable2 if condition2 ...
             for itemN in iterableN if conditionN ]

```

```
# equivalent for loop statement
for item1 in iterable1:

```

```
    if condition1:
        for item2 in iterable2:

```

```
            if condition2:
                ...

```

```
                   for itemN in iterableN:
                       if conditionN:

```

expression

88

This gives us an idea of how similar comprehensions are to looping constructs. Thebenefit we get is that they are more efficient and perform better than loops. Some caveatsinclude that you cannot use assignment statements in comprehensions because, if youremember the syntax from earlier, they support only expressions and not statements. Thesame syntax is used by set and dictionary comprehensions too.

The following examples illustrate the use of different comprehensions:

```
이것은 우리에게 유사한 구조가 루핑 구조와 얼마나 유사한지를 알려줍니다. 우리가 얻을 수있는 이점은 루프보다 효율적이고 성능이 뛰어나다는 것입니다. 일부주의 사항은 이전 구문을 기억하지 않으면 표현식 만 지원하고 구문은 지원하지 않기 때문에 구문에 할당 문을 사용할 수 없다는 점을 포함합니다. 같은 구문은 집합과 사전의 내포물에서도 사용됩니다.

다음 예는 다른 이해의 사용을 설명합니다.
```



```
In [355]: numbers = range(6)
In [356]: numbers
Out[356]: [0, 1, 2, 3, 4, 5]

```

```
# simple list comprehension to compute squares
In [357]: [num*num for num in numbers]
Out[357]: [0, 1, 4, 9, 16, 25]

```

```
# list comprehension to check if number is divisible by 2
In [358]: [num%2 for num in numbers]
Out[358]: [0, 1, 0, 1, 0, 1]

```

```
# set comprehension returns distinct values of the above operation
In [359]: set(num%2 for num in numbers)
Out[359]: {0, 1}

```

```
# dictionary comprehension where key:value is number: square(number)
In [361]: {num: num*num for num in numbers}
Out[361]: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

```

```
# a more complex comprehension showcasing above operations in a single
comprehension
In [362]: [{'number': num,

```

```
            'square': num*num,
            'type': 'even' if num%2 == 0 else 'odd'} for num in numbers]

```

```
Out[362]:
[{'number': 0, 'square': 0, 'type': 'even'},

```

```
 {'number': 1, 'square': 1, 'type': 'odd'},
 {'number': 2, 'square': 4, 'type': 'even'},
 {'number': 3, 'square': 9, 'type': 'odd'},
 {'number': 4, 'square': 16, 'type': 'even'},
 {'number': 5, 'square': 25, 'type': 'odd'}]

```

```
# nested list comprehension - flattening a list of lists
In [364]: list_of_lists = [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]]
In [365]: list_of_lists
Out[365]: [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]]
In [367]: [item for each_list in list_of_lists for item in each_list]
Out[367]: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
```

###Generators

Generators are powerful, memory-efficient constructs for creating and consumingiterators. They exist in two variants: functions and expressions. Generators work on aconcept known as lazy evaluation—hence, they are more memory efficient and performbetter in most cases because they do not require the entire object to be evaluated

and loaded in one go, as in list comprehensions. However, the caveat is that becausegenerators yield one item at a time in an ad hoc fashion, there is a chance that they mayperform worse in terms of execution time compared to list comprehensions, unless youare dealing with large objects with many elements.

Generator functions are implemented as regular functions using the def statement.However, they use the concept of lazy evaluation and return one object at a time usingthe yield statement. Unlike regular functions that have a return statement, which onceexecuted ends the execution of the code block inside the function, generators use theyield statement, which suspends and resumes execution and the state after generatingand returning each value or object. To be more precise, generator functions yield valuesat each step rather than returning them. This ensures that the current state includinginformation about the local code block scope it retained and enables the generator toresume from where it left off.

The following snippet shows some examples for generator functions:

```
생성기는 지터를 만들고 소비하는 강력하고 메모리 효율적인 구조입니다. 함수와 표현식의 두 가지 변종이 존재합니다. 생성자는 lazy evaluation으로 알려진 aconcept에서 작동합니다. 따라서 전체 객체를 평가할 필요가 없기 때문에 대부분의 경우 메모리 효율성과 성능이 향상됩니다.

list comprehensions 에서처럼 한 번에로드됩니다. 그러나,주의해야 할 점은 한 번에 하나의 항목을 임의의 방식으로 생성하기 때문에 많은 요소가있는 큰 개체를 다루지 않는 한 목록 작성 시간에 비해 실행 시간면에서 더 나쁠 수 있다는 것입니다.

생성자 함수는 def 문을 사용하여 일반 함수로 구현됩니다. 그러나 그들은 지연 성 개념을 사용하고 yield 문을 사용하여 한 번에 하나의 객체를 반환합니다. 함수 내에서 코드 블록의 실행을 종료 한 return 문을 가진 일반 함수와 달리 생성자는 각 값 또는 객체를 생성 및 반환 한 후 실행 및 상태를 일시 중단하고 다시 시작합니다. 보다 정확하게 말하면, 생성자 함수는 각 단계마다 값을 반환하지만 반환하지는 않습니다. 이렇게하면 로컬 코드 블록 범위에 대한 정보가 포함 된 현재 상태가 유지되고 생성기가 중단 된 부분부터 다시 시작할 수 있습니다.

다음 스 니펫은 생성자 함수에 대한 몇 가지 예를 보여줍니다.
```



```
In [369]: numbers = [1, 2, 3, 4, 5]

```

```
In [370]: def generate_squares(numbers):
     ...:     for number in numbers:
     ...:         yield number*number

```

```
In [371]: gen_obj = generate_squares(numbers)
In [372]: gen_obj
Out[372]: <generator object generate_squares at 0x000000000F2FC2D0>
In [373]: for item in gen_obj:

```

```
     ...:     print item

```

...:1

491625

The advantages of these generators are both memory efficiency and execution time,especially when iterables and objects are large in size and occupy substantial memory.You also do not need to load whole objects into the main memory for performing variousoperations on them. They often work very well on streaming data where you cannot keepall the data in memory at all times. The same applies for generator expressions, which arevery similar to comprehensions except they are enclosed in parentheses.

The following example illustrates:

```
이러한 생성기의 장점은 특히 메모리와 객체가 크기가 크고 많은 양의 메모리를 차지하는 경우 메모리 효율성과 실행 시간입니다. 또한 다양한 객체를 메인 메모리에로드 할 필요가 없습니다. 이들은 종종 데이터를 메모리에 보관할 수없는 스트리밍 데이터에서 항상 잘 작동합니다. 생성자 표현식에 대해서도 동일하게 적용됩니다. 생성자 표현식은 괄호로 묶인 것을 제외하고는 이해력과 매우 유사합니다.

다음 예제는 다음을 보여줍니다.
```



```
In [381]: csv_string = 'The,fox,jumps,over,the,dog'

```

```
# making a sentence using list comprehension
In [382]: list_cmp_obj = [item for item in csv_string.split(',')]
In [383]: list_cmp_obj
Out[383]: ['The', 'fox', 'jumps', 'over', 'the', 'dog']
In [384]: ' '.join(list_cmp_obj)
Out[384]: 'The fox jumps over the dog'

```

```
# making a sentence using generator expression
In [385]: gen_obj = (item for item in csv_string.split(','))
In [386]: gen_obj
Out[386]: <generator object <genexpr> at 0x000000000F2FC3F0>
In [387]: ' '.join(gen_obj)
Out[387]: 'The fox jumps over the dog'

```

Both generator functions and expressions create generator objects that use the sameconstruct as iterators and starts, stops, and resumes the function or loop at each stage,and once it is completed it raises the StopIteration exception.

```
생성자 함수와 표현식 모두 sameconstruct를 반복자로 사용하는 생성자 객체를 만들고 각 단계에서 함수 또는 루프를 시작, 중지 및 재개합니다. 완료되면 StopIteration 예외를 발생시킵니다.
```



### The itertools and functools Modules

Various modules which are available in the Python standard library. Some of the popularones include collections, itertools, and functools, which have various constructs andfunctions that can be used to boost productivity and reduce time spent writing extra codeto solve problems. The itertools module is a complete module dedicated to building andoperating on iterators. It has various functions that support different operations includingslicing, chaining, grouping, and splitting iterators. The most comprehensive source ofinformation for itertools is available in the official Python documentation at https://docs.python.org/2/library/itertools.html. The documentation lists each functionand its role with examples. The functools module provides with functions, which enableconcepts from functional programming, including wrappers and partials. These functionsusually act on other functions, which it takes as input parameters and often returns afunction as the result itself. The official documentation at https://docs.python.org/2/library/functools.html provides extensive information on each function.

```
파이썬 표준 라이브러리에서 사용할 수있는 다양한 모듈. 일부 인기 모델에는 컬렉션, itertools 및 functools가 포함되어 있습니다.이 도구는 생산성을 높이고 추가 코드 작성에 소요되는 시간을 줄이기 위해 사용할 수있는 다양한 구조 및 기능을 가지고 있습니다. itertools 모듈은 이터레이터를 구축하고 운영하기위한 완벽한 모듈입니다. 그것은 슬라이싱, 체이닝, 그룹핑 및 반복자를 포함한 다양한 연산을 지원하는 다양한 함수를 가지고 있습니다. itertools에 대한 가장 포괄적 인 정보 소스는 공식 Python 문서 (https://docs.python.org/2/library/itertools.html)에 있습니다. 설명서에는 각 기능과 그 역할이 예제와 함께 나열되어 있습니다. functools 모듈은 래퍼 (wrapper) 및 부분 (partial)을 포함한 함수 프로그래밍의 개념을 가능하게하는 함수를 제공합니다. 이러한 함수는 일반적으로 다른 함수에 작용하며 입력 매개 변수로 사용되며 종종 결과 자체로서 함수를 반환합니다. https://docs.python.org/2/library/functools.html의 공식 문서는 각 기능에 대한 광범위한 정보를 제공합니다.
```



##Classes

Python classes are constructs that enable us to write code following the OOP paradigm.Concepts like objects, encapsulation, methods, inheritance, and polymorphism are heavilyused in this paradigm. If you have worked on any OOP language before, like C++ or Java,chances are you will find using Python classes relatively similar to using classes in otherlanguages. Discussing each concept would be beyond the scope of this book, but I will brieflycover the basic concepts of classes and touch up on different types of objects and inheritance.

Classes are basically a software model or abstraction of real-world entities that
are objects. This abstraction leads to classes being called as a user-defined type, and
once you define a class, you can instantiate and create instances or objects of that class.
Each object has its own instance variables and methods that define the properties and
behavior of that object. All classes inherit from the base object type, and you can create
your own classes and inherit further classes from these user-defined classes. Classes are
also ultimately objects on their own and can be bound to variables and other constructs.

The following snippet gives the basic syntax for a class:

```
파이썬 클래스는 객체, 캡슐화, 메소드, 상속, 다형성과 같은 개념이이 패러다임에서 많이 사용된다. C ++이나 Java와 같은 OOP 언어를 사용하기 전에 다른 언어로 클래스를 사용하는 것과 비슷한 Python 클래스를 사용할 수 있습니다. 각 개념에 대해 논의하는 것은이 책의 범위를 벗어나지 만 클래스의 기본 개념을 간략하게 살펴보고 다양한 유형의 객체와 상속에 대해 설명합니다.

클래스는 기본적으로 객체 인 실제 엔티티의 소프트웨어 모델 또는 추상화입니다. 이러한 추상화로 인해 클래스가 사용자 정의 유형으로 호출되며, 일단 클래스를 정의하면 해당 클래스의 인스턴스 또는 객체를 인스턴스화하고 작성할 수 있습니다.

각 객체에는 해당 객체의 속성과 동작을 정의하는 고유 한 인스턴스 변수와 메서드가 있습니다. 모든 클래스는 기본 객체 유형을 상속하며 사용자 고유의 클래스를 만들고 이러한 사용자 정의 클래스에서 추가 클래스를 상속 할 수 있습니다. 클래스는 궁극적으로는 자체적으로 객체이며 변수 및 기타 구문에 바인딩 될 수 있습니다.

다음 스 니펫은 클래스의 기본 구문을 제공합니다.
```



```
class ClassName(BaseClass):
    class_variable  # shared by all instances\objects

```

```
    def __init__(self, ...): # the constructor
        # instance variables unique to each instance\object
        self.instance_variables = ...
```

```
    def __str__(self):  # string representation of the instance\object
        return repr(self)

```

```
    def methods(self, ...):  # instance methods
        <code block>

```

The preceding snippet tells us that the class named ClassName inherits from
its parent class BaseClass. There can be more than one parent or base class in the
parameters separated by commas. The __init__() method acts as a constructor
that instantiates and creates an object of the class using the call ClassName(...),
which automatically invokes the __init__() method—which may optionally take
parameters based on its definition. The __str__() method is optional. It prints the string
representation of the object. You can modify the default method with your own definition,
and it is often used to print the current state of the object variables. The class_variable
indicates class variables that are defined in the block just enclosing the class definition,
and these class variables are shared by all objects or instances of the class. The instance_
variables are variables that are specific to each object or instance. The methods denote
instance methods that define specific behavior of the objects. The self parameter is
usually used as the first parameter in methods, which is more of a convention that refers
to the instance or object of ClassName on which you call the method.

The following example depicts a simple class and how it works:

```
앞의 스 니펫은 ClassName이라는 클래스가 상위 클래스 인 BaseClass를 상속 받았다고 알려줍니다. 쉼표로 구분 된 매개 변수에는 둘 이상의 상위 또는 기본 클래스가있을 수 있습니다. init () 메소드는 자동으로 init () 메소드를 호출하는 ClassName (...) 호출을 사용하여 클래스의 객체를 인스턴스화하고 생성하는 생성자 역할을 수행합니다.이 메소드는 선택적으로 정의에 따라 매개 변수를 취할 수 있습니다. str () 메서드는 선택 사항입니다. 객체의 문자열 표현을 인쇄합니다. 사용자 정의를 사용하여 기본 메소드를 수정할 수 있으며, 이는 종종 오브젝트 변수의 현재 상태를 인쇄하는 데 사용됩니다. class_variable은 클래스 정의를 둘러싼 블록에 정의 된 클래스 변수를 나타내며이 클래스 변수는 클래스의 모든 객체 또는 인스턴스에서 공유됩니다. instance_variables는 각 객체 또는 인스턴스에 고유 한 변수입니다. 메서드는 개체의 특정 동작을 정의하는 인스턴스 메서드를 나타냅니다. self 매개 변수는 대개 메서드의 첫 번째 매개 변수로 사용되며,이 메서드는 메서드를 호출하는 ClassName의 인스턴스 또는 개체를 참조하는 규칙입니다.

다음 예제는 간단한 클래스와 그 작동 방식을 보여줍니다.
```



```
# class definition
In [401]: class Animal(object):

```

- ```
       ...:      species = 'Animal'
       ...:
   ```

  ```

- ```
       ...:      def __init__(self, name):

  ```

- ```
       ...:          self.name = name
   ```

  ```

- ```
       ...:          self.attributes = []
       ...:

  ```

- ```
       ...:      def add_attributes(self, attributes):
   ```

  ```

- ```
       ...:          self.attributes.extend(attributes) \

  ```

92

```
...:
...:
...:
...:
...:

```

...:

```
        if type(attributes) == list \
        else self.attributes.append(attributes)

```

```
def __str__(self):
    return self.name+" is of type "+self.species+" and has
    attributes:"+str(self.attributes)

```

```
# instantiating the class
In [402]: a1 = Animal('Rover')
# invoking instance method
In [403]: a1.add_attributes(['runs', 'eats', 'dog'])
# user defined string representation of the Animal class
In [404]: str(a1)
Out[404]: "Rover is of type Animal and has attributes:['runs', 'eats',

```

'dog']"

This gives us an idea of how classes work. But what if we want to target specificanimals like dogs and foxes? We can apply the concept of inheritance and use the super()method to access the constructor of the base Animal class in each definition. Thefollowing examples illustrate the concept of inheritance:

```
이렇게하면 수업이 어떻게 작동하는지 알 수 있습니다. 그러나 개와 여우 같은 특정 동물을 타겟팅하고 싶다면 어떻게해야할까요? 상속 개념을 적용하고 super () 메서드를 사용하여 각 정의에서 기본 Animal 클래스의 생성자에 액세스 할 수 있습니다. 다음 예제는 상속의 개념을 보여줍니다.
```



```
# deriving class Dog from base class Animal
In [413]: class Dog(Animal):

```

```
...:
...:
...:
...:

```

```
species = 'Dog'

```

```
def __init__(self, *args):
    super(Dog, self).__init__(*args)

```

```
# deriving class Fox from base class Animal
In [414]: class Fox(Animal):

```

```
...:
...:
...:
...:

```

```
species = 'Fox'

```

```
def __init__(self, *args):
    super(Fox, self).__init__(*args)

```

```
# creating instance of class Dog
In [415]: d1 = Dog('Rover')
In [416]: d1.add_attributes(['lazy', 'beige', 'sleeps', 'eats'])
In [417]: str(d1)
Out[417]: "Rover is of type Dog and has attributes:['lazy', 'beige',

```

```
          'sleeps', 'eats']"

```

```
# creating instance of class Fox
In [418]: f1 = Fox('Silver')
In [419]: f1.add_attributes(['quick', 'brown', 'jumps', 'runs'])
In [420]: str(f1)
Out[420]: "Silver is of type Fox and has attributes:['quick', 'brown',

```

```
          'jumps', 'runs']"
```

##Working with Text

We have seen most of the constructs, data types, structures, concepts, and programmingparadigms associated with Python in the previous sections. This section briefly coversspecific data types tailored to handle text data and shows how these data types and theirassociated utilities will be useful for us in the future chapters. The main data types used tohandle text data in Python are strings, which can be normal strings, bytes storing binaryinformation, or Unicode. By default, all strings are Unicode in Python 3.x, but they are notso in Python 2.x, and this is something you should definitely keep in mind when dealingwith text in different Python distributions. Strings are a sequence of characters in Pythonsimilar to arrays and code with a set of attributes and methods that can be leveraged tomanipulate and operate on text data easily, which makes Python the language of choicefor text analytics in many scenarios. We will discuss various types of strings with severalexamples in the next section.

```
이전 섹션에서 파이썬과 관련된 대부분의 구조, 데이터 유형, 구조, 개념 및 프로그래밍 방식을 보았습니다. 이 절에서는 텍스트 데이터를 처리하도록 특수화 된 특정 데이터 유형을 간략하게 다루고 있으며 이러한 데이터 유형과 관련 유틸리티가 향후 장에서 우리에게 유용 할 수있는 방법을 보여줍니다. 파이썬에서 텍스트 데이터를 처리하는 데 사용되는 주요 데이터 유형은 일반 문자열, 바이너리 정보를 저장하는 바이트 또는 유니 코드 일 수있는 문자열입니다. 기본적으로 모든 문자열은 Python 3.x에서 유니 코드이지만 Python 2.x에서는 그렇지 않습니다. 이것은 다른 Python 배포판의 텍스트를 처리 할 때 반드시 명심해야 할 사항입니다. 문자열은 Pythons와 비슷한 형태의 문자 배열이며, 텍스트 데이터를 쉽게 조작하고 조작 할 수있는 일련의 특성 및 메서드가 포함 된 코드이므로 여러 시나리오에서 Python을 텍스트 분석을위한 언어로 사용할 수 있습니다. 우리는 다음 섹션에서 여러 가지 예제와 함께 다양한 유형의 문자열을 논의 할 것입니다.
```



###String Literals

There are various types of strings, as mentioned earlier, and you saw a few examples inone of the previous sections regarding data types. The following BNF (Backus-Naur Form)gives us the general lexical definitions for producing strings as seen in the official Pythondocs:

```
앞에서 언급했듯이 다양한 유형의 문자열이 있으며 데이터 유형과 관련된 이전 섹션의 몇 가지 예를 보았습니다. 다음 BNF (Backus-Naur Form)는 공식 Pythondocs에서 볼 수있는 문자열 생성을위한 일반적인 어휘 정의를 제공합니다.
```

```
stringliteral
stringprefix

```

```
::=  [stringprefix](shortstring | longstring)
::=  "r" | "u" | "ur" | "R" | "U" | "UR" | "Ur" | "uR"

```

```
     | "b" | "B" | "br" | "Br" | "bR" | "BR"
::=  "'" shortstringitem* "'" | '"' shortstringitem* '"'
::=  "'''" longstringitem* "'''" | '"""' longstringitem*

```

```
shortstring
longstring
'"""'
shortstringitem ::=  shortstringchar | escapeseq
longstringitem  ::=  longstringchar | escapeseq
shortstringchar ::=  <any source character except "\" or newline or the
quote>

```

```
longstringchar  ::=  <any source character except "\">
escapeseq       ::=  "\" <any ASCII character>

```

The preceding rules tell us that different types of string prefixes exist that can be usedwith different string types to produce string literals. In simple terms, the following types ofstring literals are used the most:

- Short strings: These strings are usually enclosed with single (') ordouble quotes (") around the characters. Some examples wouldbe, 'Hello' and "Hello".
- Long strings: These strings are usually enclosed with threesingle (''') or double quotes (""") around the characters. Someexamples would be, """Hello, I’m a long string""" or'''Hello I\’m a long string '''. Note the (\’), indicates anescape sequence discussed in the next bullet.


- Escape sequences in strings: These strings often have escapesequences embedded in them, where the rule for escapesequences starts with a backslash (\) followed by any ASCIIcharacter. Hence, they perform backspace interpolation. Popularescape sequences include (\n), indicating a new line character,and (\t), indicating a tab.

- Bytes: These are used to represent bytestrings, which createobjects of the bytes data type. These strings can be created asbytes('...') or using the b'...' notation. Examples would bebytes('hello') and b'hello'.

- Raw strings: These strings were originally created specifically forregular expressions (regex) and creating regex patterns. Thesestrings can be created using the r'...' notation and keep thestring in its raw or native form. Hence, it does not perform anybackspace interpolation and turns off the escape sequences. Anexample would be r'Hello'.

- Unicode: These strings support Unicode characters in text andare usually non-ASCII character sequences. These strings aredenoted with the u'...' notation. Besides the string notation,there are several specific ways to represent special Unicodecharacters in the string. The usual include the hex byte valueescape sequence of the format '\xVV'. Besides this, we alsohave Unicode escape sequences of the form '\uVVVV' and '\uVVVVVVVV', where the first form uses 4 hex-digits for encodinga 16-bit character, and the second uses 8 hex digits for encodinga32-bitcharacter.Someexampleswouldbeu 'H\xe8llo'andu'H\u00e8llo' which represents the string 'Hèllo'.

  The following code snippet depicts these different types of string literals and theiroutput :

  ```
  앞의 규칙은 문자열 리터럴을 생성하기 위해 다른 문자열 유형과 함께 사용할 수있는 다양한 유형의 문자열 접두사가 있음을 알려줍니다. 간단히 말해, 다음 유형의 문자열 리터럴이 가장 많이 사용됩니다.

  - 짧은 문자열 : 보통이 문자열은 문자 주위에 작은 따옴표 ( ")로 묶여 있으며, 일부 예로 'Hello'와 'Hello'가 있습니다.

  - 긴 문자열 :이 문자열은 일반적으로 문자 주위에 3 자릿수 ( '' ') 또는 큰 따옴표 ( "" ")로 묶입니다. 예를 들어," ""안녕하세요, 저는 긴 문자열입니다. ""또는 "' ' 안녕하세요, 저는 긴 문자열 '' '입니다. (\')는 다음 글 머리 기호에서 설명하는 anescape 시퀀스를 나타냅니다.

  - 문자열의 이스케이프 시퀀스 : 이스케이프 시퀀스 규칙에는 이스케이프 시퀀스가 백 슬래시 ()와 ASCII 문자로 시작하는 이스케이프 시퀀스가 포함되어있는 경우가 많습니다. 따라서 백 스페이스 보간을 수행합니다.
  Popularescape 시퀀스에는 새 줄 문자를 나타내는 (\ n)과 탭을 나타내는 (\ t)가 포함됩니다.

  - Bytes : 바이트 데이터 유형의 오브젝트를 작성하는 bytestrings을 나타내는 데 사용됩니다. 이 문자열은 asbytes ( '...') 또는 b '...'표기법을 사용하여 만들 수 있습니다. 예는 bebytes ( 'hello')와 b'hello '입니다.

  - 원시 문자열 :이 문자열은 원래 정규식 (정규식) 및 정규식 패턴 작성을 위해 특별히 작성되었습니다. Thesestrings은 r '...'표기법을 사용하여 만들 수 있으며 문자열을 원시 또는 원시 형식으로 유지할 수 있습니다. 따라서 backspace 공간 보간을 수행하지 않고 이스케이프 시퀀스를 끕니다. 예를 들어 r'Hello '입니다.

  - 유니 코드 :이 문자열은 텍스트에서 유니 코드 문자를 지원하며 일반적으로 비 ASCII 문자 시퀀스입니다. 이 문자열에는 u '...'표기법이 사용됩니다. 문자열 표기법 외에도 문자열에 특수 유니 코드 문자를 표시하는 몇 가지 특정 방법이 있습니다. 보통 '\ xVV'형식의 16 진수 바이트 값 이스케이프 시퀀스가 포함됩니다. 이 외에도 '\ uVVVV'및 '\ uVVVVVVV'형식의 유니 코드 이스케이프 시퀀스가 있습니다. 첫 번째 형식은 16 비트 문자를 인코딩 할 때 4 자리 16 진수를 사용하고 두 번째 형식은 8 진수를 encodinga32-bitcharacter 인코딩에 사용합니다. 예를 들어 'H \ xe8llo'andu'H \ u00e8llo'는 'Hèllo'문자열을 나타냅니다. 다음 코드 스 니펫은 이러한 다양한 유형의 문자열 리터럴과 theiroutput을 보여줍니다.
  ```

  ```
  # simple string
  In [422]: simple_string = 'hello' + " I'm a simple string"
  In [423]: print simple_string
  hello I'm a simple string

  # multi-line string, note the \n (newline) escape character automatically
  created
  In [424]: multi_line_string = """Hello I'm

  ```

  ```
       ...: a multi-line

  ```

  ```
       ...: string!"""
  In [425]: multi_line_string
  Out[425]: "Hello I'm\na multi-line\nstring!"
  In [426]: print multi_line_string
  Hello I'm
  a multi-line
  string!
  ```

```
# Normal string with escape sequences leading to a wrong file path!
In [427]: escaped_string = "C:\the_folder\new_dir\file.txt"
In [428]: print escaped_string  # will cause errors if we try to open a file

```

```
          here
C:      he_folder

```

```
ew_dirile.txt

```

```
# raw string keeping the backslashes in its normal form
In [429]: raw_string = r'C:\the_folder\new_dir\file.txt'
In [430]: print raw_string
C:\the_folder\new_dir\file.txt

```

```
# unicode string literals
In [431]: string_with_unicode = u'H\u00e8llo!'

```

```
     ...: print string_with_unicode
Hèllo!

```

###String Operations and Methods

Strings are iterable sequences, which means a lot of operations can be performed onthem, useful especially when processing and parsing textual data into easy-to-consumeformats. Several operations can be performed on strings. I have categorized them into thefollowing segments:

- Basic operations
- Indexing and slicing
- Methods
- Formatting
- Regular expressions

These would cover the most frequently used techniques for working with strings andform the base of what we would need to get started in the next chapter (where we look atunderstanding and processing textual data based on concepts we learned in the first twochapters).

Basic Operations

You can perform several basic operations on strings, including concatenation andchecking for substrings, characters, and lengths. The following code snippet illustratesthese operations with some examples:

```
문자열은 반복 가능한 시퀀스입니다. 즉, 많은 작업을 수행 할 수 있습니다. 특히 텍스트 데이터를 쉽게 처리하고 구문 분석하여 사용하기 쉬운 형식으로 만들 때 유용합니다. 문자열에 대해 여러 작업을 수행 할 수 있습니다. 나는 그 (것)들을 뒤에 오는 세그먼트로 분류했다 :

- 기본 조작
- 인덱싱 및 분할
- 방법
- 서식 지정
- 정규 표현식

이것들은 문자열 작업을 위해 가장 많이 사용되는 기술을 다루며 다음 장에서 시작해야 할 것들의 기초를 형성 할 것입니다 (우리는 처음 두 장에서 배운 개념을 기반으로 텍스트 데이터를 이해하고 처리하는 것을 보았습니다).

기본 작업

하위 문자열, 문자 및 길이에 대한 연결 및 검사를 비롯하여 문자열에 대한 몇 가지 기본 작업을 수행 할 수 있습니다. 다음 코드 스니 j은 몇 가지 예제로 조작을 설명합니다.
```

```
# Different ways of String concatenation
In [436]: 'Hello' + ' and welcome ' + 'to Python!'
Out[436]: 'Hello and welcome to Python!'
In [437]: 'Hello' ' and welcome ' 'to Python!'
Out[437]: 'Hello and welcome to Python!'

# concatenation of variables and literals
In [438]: s1 = 'Python!'
In [439]: 'Hello ' + s1
Out[439]: 'Hello Python!'

# we cannot concatenate a variable and a literal using this method
In [440]: 'Hello ' s1

  File "<ipython-input-440-2f801ddf3480>", line 1
    'Hello ' s1
              ^
SyntaxError: invalid syntax

# some more ways of concatenating strings
In [442]: s2 = '--Python--'
In [443]: s2 * 5
Out[443]: '--Python----Python----Python----Python----Python--'
In [444]: s1 + s2

Out[444]: 'Python!--Python--'
In [445]: (s1 + s2)*3
Out[445]: 'Python!--Python--Python!--Python--Python!--Python--'

# concatenating several strings together in parentheses
In [446]: s3 = ('This '
       ...:        'is another way '
       ...:        'to concatenate '
       ...:        'several strings!')
  In [447]: s3
  Out[447]: 'This is another way to concatenate several strings!'

# checking for substrings in a string
  In [448]: 'way' in s3
  Out[448]: True
  In [449]: 'python' in s3
  Out[449]: False
# computing total length of the string
  In [450]: len(s3)
  Out[450]: 51
```

  Indexing and Slicing

  As mentioned, strings are iterables—ordered sequences of characters. Hence they canbe indexed, sliced, and iterated through similarly to other iterables such as lists. Eachcharacter has a specific position in the string, called its index. Using indexes, we canaccess specific parts of the string. Accessing a single character using a specific positionor index in the string is called indexing, and accessing a part of a string, for example,

  a substring using a start and end index, is called slicing. Python supports two types of

indexes. One starts from 0 and increases by 1 each time per character till the end of thestring. The other starts from –1 at the end of the string and decreases by 1 each time foreach character till the beginning of the string. Figure 2-6 shows the two types of indexesfor the string 'PYTHON'.

Figure2-6. Stringindexingsyntax

To access any particular character in the string, you need to use the correspondingindex, and slices can be extracted using the syntax var[start:stop], which extracts allcharacters in the string var from index start till index stop excluding the character at thestop index.

The following examples shows how to index, slice, and iterate through strings:

```
인덱싱 및 분할

  앞서 언급했듯이 문자열은 반복 가능한 순서로 정렬 된 문자 시퀀스입니다. 따라서 목록과 같은 다른 iterable과 유사하게 인덱싱, 슬라이스 및 반복 될 수 있습니다. 각 문자는 색인이라는 특정 위치를 문자열에 가지고 있습니다. 인덱스를 사용하여 문자열의 특정 부분을 액세스 할 수 있습니다. 문자열의 특정 위치 또는 인덱스를 사용하여 단일 문자에 액세스하는 것을 인덱싱이라고하며, 시작 및 끝 인덱스를 사용하는 하위 문자열과 같이 문자열의 일부에 액세스하는 것을 슬라이싱이라고합니다. 파이썬은 두 가지 유형의 인덱스를 지원합니다. 하나는 0부터 시작하여 문자열 당 끝까지 1 씩 증가합니다. 다른 하나는 문자열의 끝에서 -1부터 시작하여 매번 foreach 문자가 문자열의 시작 부분까지 매번 1 씩 감소합니다. 그림 2-6은 'PYTHON'문자열에 대한 두 가지 유형의 색인을 보여줍니다.

그림 2-6. Stringindexingsyntax

문자열의 특정 문자에 액세스하려면 해당 색인을 사용해야하며, 문자열 var의 모든 문자를 색인 start에서 색인 추출까지 중지 코드에서 제외하는 구문 var [start : stop]을 사용하여 슬라이스를 추출 할 수 있습니다. .

다음 예제는 문자열을 인덱싱, 슬라이스 및 반복하는 방법을 보여줍니다.
```

  ```
# creating a string
In [460]: s = 'PYTHON'

  ```

```
# depicting string indexes
In [461]: for index, character in enumerate(s):

```

```
     ...:     print 'Character', character+':', 'has index:', index
Character P: has index: 0
Character Y: has index: 1
Character T: has index: 2

```

```
Character H: has index: 3
Character O: has index: 4
Character N: has index: 5

```

```
# string indexing
In [462]: s[0], s[1], s[2], s[3], s[4], s[5]
Out[462]: ('P', 'Y', 'T', 'H', 'O', 'N')
In [463]: s[-1], s[-2], s[-3], s[-4], s[-5], s[-6]
Out[463]: ('N', 'O', 'H', 'T', 'Y', 'P')

```

```
# string slicing
In [464]: s[:]
Out[464]: 'PYTHON'
In [465]: s[1:4]
Out[465]: 'YTH'

```

```
In [466]: s[:3]
Out[466]: 'PYT'
In [467]: s[3:]
Out[467]: 'HON'

```

```
# prints whole string when no indexes are specified

```

98

```
In [468]: s[-3:]
Out[468]: 'HON'
In [469]: s[:3] + s[3:]
Out[469]: 'PYTHON'
In [470]: s[:3] + s[-3:]
Out[470]: 'PYTHON'

```

```
# string slicing with offsets
In [472]: s[::1]  # no offset
Out[472]: 'PYTHON'
In [473]: s[::2]  # print every 2nd character in string
Out[473]: 'PTO'

```

```
# strings are immutable hence assignment throws error
In [476]: s[0] = 'X'
Traceback (most recent call last):

```

```
  File "<ipython-input-476-2cd5921aae94>", line 1, in <module>
    s[0] = 'X'

```

```
TypeError: 'str' object does not support item assignment

```

```
# creates a new string
In [477]: 'X' + s[1:]
Out[477]: 'XYTHON'

```

Methods

Strings and Unicode put a huge arsenal of built-in methods at your disposal, which
you can use for performing various transformations, manipulations, and operations on
strings. Although discussing each method in detail would be beyond the current scope,
the official Python documentation at https://docs.python.org/2/library/stdtypes.
html#string-methods provides all the information you need about each and every
method, along with syntax and definitions. Methods are extremely useful and increase
your productivity because you do not have to spend extra time writing boilerplate code to
handle and manipulate strings.

The following code snippets show some popular examples of string methods inaction:

```
행동 양식

문자열과 유니 코드는 다양한 변형, 조작 및 문자열에 대한 작업을 수행하는 데 사용할 수있는 내장 된 방법을 제공합니다. 각 메서드에 대해 자세히 논의하는 것은 현재 범위를 벗어나지 만 공식 Python 설명서는 https://docs.python.org/2/library/stdtypes에 나와 있습니다.

html # string-methods는 구문 및 정의와 함께 모든 메소드에 대해 필요한 모든 정보를 제공합니다. 메서드는 매우 유용하며 문자열을 처리하고 조작하기위한 상용구 코드를 작성하는 데 시간을 추가 할 필요가 없기 때문에 생산성을 높일 수 있습니다.

다음 코드 스 니펫은 사용되지 않는 문자열 메소드의 일반적인 예를 보여줍니다.
```



```
# case conversions
In [484]: s = 'python is great'
In [485]: s.capitalize()
Out[485]: 'Python is great'
In [486]: s.upper()
Out[486]: 'PYTHON IS GREAT'

```

```
# string replace
In [487]: s.replace('python', 'analytics')
Out[487]: 'analytics is great'
```

```
# string splitting and joining
In [488]: s = 'I,am,a,comma,separated,string'
In [489]: s.split(',')
Out[489]: ['I', 'am', 'a', 'comma', 'separated', 'string']
In [490]: ' '.join(s.split(','))
Out[490]: 'I am a comma separated string'

```

```
# stripping whitespace characters
In [497]: s = '   I am surrounded by spaces    '
In [498]: s
Out[498]: '   I am surrounded by spaces    '
In [499]: s.strip()
Out[499]: 'I am surrounded by spaces'

```

```
# coverting to title case
In [500]: s = 'this is in lower case'
In [501]: s.title()
Out[501]: 'This Is In Lower Case'

```

The preceding examples just scratch the surface of the numerous manipulationsand operations possible on strings. Feel free to try out other operations using differentmethods mentioned in the docs. We will use several of them in subsequent chapters.

Formatting

String formatting is used to substitute specific data objects and types in a string. Thisis mostly used when displaying text to the user. There are mainly two different types offormatting used for strings:

- Formatting expressions: These expressions are typically of thesyntax'...%s...%s...' %(values),wherethe%sdenotesaplaceholder for substituting a string from the list of strings depictedin values. This is quite similar to the C style printf model and hasbeen there in Python since the beginning. You can substitute valuesof other types with the respective alphabet following the % symbol,like %d for integers and %f for floating point numbers.

- Formatting methods: These strings take the form of '...{}...
  {}...'.format(values), which makes use of the braces {}
  for placeholders to place strings from values using the format
  method. These have been present in Python since version 2.6.x.

  The following code snippets depict both types of string formatting using severalexamples:

```
위의 예제는 수많은 조작과 문자열에서 가능한 작업의 표면을 긁어 모았습니다. 문서에서 언급 된 다른 방법을 사용하여 다른 작업을 사용해보십시오. 다음 장에서 몇 가지를 사용할 것입니다.

서식 지정

문자열 서식 지정은 특정 데이터 개체와 문자열을 문자열로 대체하는 데 사용됩니다. 이것은 주로 사용자에게 텍스트를 표시 할 때 사용됩니다. 주로 문자열에 사용되는 두 가지 유형의 서식이 있습니다.

- 형식화 표현식 :이 표현식은 일반적으로 '... % s ... % s ...'% (값) 구문을 사용합니다. 여기서 % s는 값으로 표시된 문자열 목록의 문자열을 대체하기위한 자리 표시 자입니다. 이것은 C 스타일의 printf 모델과 매우 비슷하며 처음부터 파이썬에서 사용되었습니다. 정수의 경우 % d, 부동 소수점 숫자의 경우 % f와 같은 % 기호 다음의 각 알파벳으로 다른 유형의 값을 대체 할 수 있습니다.
- 형식화 방법 :이 문자열은 '... {} ...'의 형식을 취합니다.
  {} ... '. 형식 (값) : 중괄호 {}를 사용합니다.
  형식을 사용하여 값에서 문자열을 배치하는 자리 표시 자
  방법. 이것들은 2.6.x 이후의 Python에 존재합니다.
  다음 코드 조각은 여러 예제를 사용하여 두 가지 유형의 문자열 서식을 보여줍니다.
```

```
  # simple string formatting expressions
  In [506]: 'Hello %s' %('Python!')
  Out[506]: 'Hello Python!'
```

  ```
In [507]: 'Hello %s' %('World!')
Out[507]: 'Hello World!'

  ```

```
# formatting expressions with different data types
In [508]: 'We have %d %s containing %.2f gallons of %s' %(2, 'bottles', 2.5,

```

```
          'milk')
Out[508]: 'We have 2 bottles containing 2.50 gallons of milk'
In [509]: 'We have %d %s containing %.2f gallons of %s' %(5, 'jugs', 10.867,

```

```
          'juice')
Out[509]: 'We have 5 jugs containing 10.87 gallons of juice'

```

```
# formatting using the format method
In [511]: 'Hello {} {}, it is a great {} to meet you'.format('Mr.', 'Jones',

```

```
          'pleasure')
Out[511]: 'Hello Mr. Jones, it is a great pleasure to meet you'
In [512]: 'Hello {} {}, it is a great {} to meet you'.format('Sir',

```

```
          'Arthur', 'honor')
Out[512]: 'Hello Sir Arthur, it is a great honor to meet you'

```

```
# alternative ways of using format
In [513]: 'I have a {food_item} and a {drink_item} with me'.format(drink_

```

```
          item='soda', food_item='sandwich')
Out[513]: 'I have a sandwich and a soda with me'
In [514]: 'The {animal} has the following attributes: {attributes}'.

```

```
          format(animal='dog', attributes=['lazy', 'loyal'])
Out[514]: "The dog has the following attributes: ['lazy', 'loyal']"

```

From the preceding examples, you can see that there is no hard-and-fast rule forformatting strings, so go ahead and experiment with different formats and use the onebest suited for your task.

Regular Expressions (Regexes)

Regular expressions, also called regexes, allow you to create string patterns and use themfor searching and substituting specific pattern matches in textual data. Python offers arich module named re for creating and using regular expressions. Entire books have beenwritten on this topic because it is easy to use but difficult to master. Discussing everyaspect of regular expressions would not be possible in these pages, but I will cover themain areas with sufficient examples.

Regular expressions or regexes are specific patterns often denoted using the
raw string notation. These patterns match a specific set of strings based on the rules
expressed by the patterns. These patterns then are usually compiled into bytecode that is
then executed for matching strings using a matching engine. The re module also provides
several flags that can change the way the pattern matches are executed. Some important
flags include the following:

```
앞의 예제에서 문자열 서식 지정을위한 쉽고 빠른 규칙이 없다는 것을 알 수 있으므로 다른 형식으로 실험하고 작업에 적합한 onebest를 사용하십시오.

정규 표현식 (정규 표현식)

regexes라고도하는 정규 표현식을 사용하면 문자열 패턴을 생성하고이를 사용하여 텍스트 데이터에서 특정 패턴 일치를 검색하고 대체 할 수 있습니다. 파이썬은 정규 표현식을 만들고 사용하기 위해 re라는 arich 모듈을 제공합니다. 사용하기 쉽지만 익히기가 어렵 기 때문에이 주제에 대해 전체 책을 썼습니다. 이 페이지에서는 정규 표현식의 모든면을 논의 할 수는 없지만 충분한 예제를 통해 주제 영역을 다룰 예정입니다.

정규 표현식 또는 정규 표현식은 종종 원시 문자열 표기법을 사용하여 표시된 특정 패턴입니다. 이 패턴은 패턴에 의해 표현 된 규칙을 기반으로 특정 문자열 세트와 일치합니다. 그런 다음이 패턴은 일반적으로 바이트 코드로 컴파일 된 다음 일치하는 엔진을 사용하여 일치하는 문자열에 대해 실행됩니다. re 모듈은 또한 패턴 일치가 실행되는 방식을 변경할 수있는 몇 가지 플래그를 제공합니다. 몇 가지 중요한 플래그는 다음과 같습니다.
```



- re.I or re.IGNORECASE is used to match patterns ignoring casesensitivity.


- re.S or re.DOTALL causes the period (.) character to match any character including new lines.

- re.U or re.UNICODE helps in matching Unicode-based charactersalso (deprecated in Python 3.x).

  For pattern matching, various rules are used in regexes. Some popular ones includethe following:


- . for matching any single character

- ^ for matching the start of the string

- $ for matching the end of the string

- \* for matching zero or more cases of the previous mentionedregex before the * symbol in the pattern

- ? for matching zero or one case of the previous mentioned regexbefore the ? symbol in the pattern

- [...] for matching any one of the set of characters inside thesquare brackets

- [^...] for matching a character not present in the squarebrackets after the ^ symbol

- | denotes the OR operator for matching either the preceding orthe next regex

- \+ for matching one or more cases of the previous mentioned regexbefore the + symbol in the pattern

- \d for matching decimal digits which is also depicted as [0-9]

- \D for matching non-digits, also depicted as [^0-9]

- \s for matching white space characters

- \S for matching non whitespace characters

- \w for matching alphanumeric characters also depicted as[a-zA-Z0-9_]

- \W for matching non alphanumeric characters also depicted as[^a-zA-Z0-9_]

Regular expressions can be compiled into pattern objects and then used with avariety of methods for pattern search and substitution in strings. The main methodsoffered by the re module for performing these operations are as follows:

- re.compile(): This method compiles a specified regularexpression pattern into a regular expression object that can beused for matching and searching. Takes a pattern and optionalflags as input, discussed earlier.
- re.match(): This method is used to match patterns at thebeginning of strings.


- re.search(): This method is used to match patterns occurring at any position in the string.

- re.findall(): This method returns all non-overlapping matchesof the specified regex pattern in the string.

- re.finditer(): This method returns all matched instances in theform of an iterator for a specific pattern in a string when scannedfrom left to right.

- re.sub(): This method is used to substitute a specified regexpattern in a string with a replacement string. It only substitutesthe leftmost occurrence of the pattern in the string.

  The following code snippets depict some of the methods just discussed and howthey are typically used when dealing with strings and regular expressions:

```
re.I 또는 re.IGNORECASE는 대문자와 소문자를 무시하는 패턴을 일치시키는 데 사용됩니다.

- re.S 또는 re.DOTALL은 마침표 (.) 문자가 새 행을 포함하여 모든 문자와 일치하도록합니다.
- re.U 또는 re.UNICODE는 유니 코드 기반 문자를 일치시키는 데에도 도움이됩니다 (Python 3.x에서는 더 이상 사용되지 않습니다).
  패턴 매칭을 위해 정규 표현식에서 다양한 규칙이 사용됩니다. 몇몇 대중적인 것은 다음을 포함합니다 :

-. 단일 문자를 매칭하기위한
- 문자열의 시작을 일치시키는 ^
- 문자열의 끝과 일치하는 $
- * 패턴에서 * 기호 앞에있는 앞에서 언급 한 정규식의 0 개 이상의 경우를 매칭하는 *
-? 이전에 언급 한 정규 표현식의 0 또는 1 개의 경우를 매칭하기 위해? 패턴의 상징
- [...] 대괄호 안의 문자 집합 중 하나와 일치하는 경우 [...]
- ^ 기호 다음에 squarebrackets에없는 문자를 일치시키는 [^ ...]
- | 앞 또는 다음 정규 표현식 중 하나와 일치하는 OR 연산자를 나타냅니다.
+ 패턴에서 + 기호 앞에 앞에서 언급 한 정규 표현식의 하나 이상의 사례를 일치시키기위한 +
- \ d는 10 진수와 일치하며 [0-9]로 표시됩니다.
- 0 ~ 9로 표시되는 숫자와 일치하지 않는 \ D
- \ s는 공백 문자를 일치시킵니다.
- \ S는 공백이 아닌 문자를 일치시킵니다.
- [a-zA-Z0-9_]로 표시된 영숫자와 일치하는 \
- 영숫자가 아닌 문자와 일치하는 \ W (aa-zA-Z0-9_로도 표시)

정규 표현식을 패턴 객체로 컴파일 한 다음 패턴 검색 및 문자열 대체를위한 다양한 메소드와 함께 사용할 수 있습니다. 이러한 작업을 수행하기 위해 re 모듈이 수행하는 기본 메소드는 다음과 같습니다.

- re.compile () :이 메소드는 지정된 정규 표현식 패턴을 일치 및 검색에 사용할 수있는 정규 표현식 객체로 컴파일합니다. 앞에서 설명한 패턴과 optionalflags를 입력으로 사용합니다.
- re.match () :이 메소드는 문자열 시작 패턴을 일치시키는 데 사용됩니다.

- re.search () :이 메소드는 문자열의 모든 위치에서 발생하는 패턴을 일치시키는 데 사용됩니다.
- re.findall () :이 메소드는 문자열에서 지정된 정규 표현식 패턴과 겹치지 않는 모든 문자열을 반환합니다.
- re.finditer () :이 메소드는 왼쪽에서 오른쪽으로 스캔 할 때 문자열의 특정 패턴에 대한 iterator의 form에 일치하는 모든 인스턴스를 리턴합니다.
- re.sub () :이 메소드는 문자열의 지정된 정규 표현식을 대체 문자열로 대체하는 데 사용됩니다. 문자열에서 가장 왼쪽에 나타나는 패턴을 대체합니다.
  다음 코드 스 니펫은 방금 설명한 방법 중 일부와 문자열 및 정규식을 처리 할 때 일반적으로 사용되는 방법을 보여줍니다.
```



```
  # importing the re module
  In [526]: import re

```

  ```
  # dealing with unicode matching using regexes
  In [527]: s = u'H\u00e8llo'
  In [528]: s
  Out[528]: u'H\xe8llo'

  ```

  ```
  In [529]: print s
  Hèllo
  # does not return the special unicode character even if it is alphanumeric
  In [530]: re.findall(r'\w+', s)
  Out[530]: [u'H', u'llo']
  # need to explicitly specify the unicode flag to detect it using regex
  In [531]: re.findall(r'\w+', s, re.UNICODE)
  Out[531]: [u'H\xe8llo']

  ```

  ```
  # setting up a pattern we want to use as a regex
  # also creating two sample strings
  In [534]: pattern = 'python'

  ```

  ```
       ...: s1 = 'Python is an excellent language'
       ...: s2 = 'I love the Python language. I also use Python to build

  ```

  ```
            applications at work!'

  ```

  ```
  # match only returns a match if regex match is found at the beginning of the
  string
  In [535]: re.match(pattern, s1)
  # pattern is in lower case hence ignore case flag helps

  ```

  ```
  # in matching same pattern with different cases
  In [536]: re.match(pattern, s1, flags=re.IGNORECASE)
  Out[536]: <_sre.SRE_Match at 0xf378308>
  ```

  ```
# printing matched string and its indices in the original string
In [537]: m = re.match(pattern, s1, flags=re.IGNORECASE)
In [538]: print 'Found match {} ranging from index {} - {} in the string
"{}"'.format(m.group(0), m.start(), m.end(), s1)
Found match Python ranging from index 0 - 6 in the string "Python is an
excellent language"

  ```

```
# match does not work when pattern is not there in the
beginning of string s2
In [539]: re.match(pattern, s2, re.IGNORECASE)

```

```
# illustrating find and search methods using the re module
In [540]: re.search(pattern, s2, re.IGNORECASE)
Out[540]: <_sre.SRE_Match at 0xf378920>

```

```
In [541]: re.findall(pattern, s2, re.IGNORECASE)
Out[541]: ['Python', 'Python']

```

```
In [542]: match_objs = re.finditer(pattern, s2, re.IGNORECASE)
In [543]: print "String:", s2

```

```
     ...: for m in match_objs:
     ...:     print 'Found match "{}" ranging from index {} - {}'.format(m.

```

```
              group(0), m.start(), m.end())
String: I love the Python language. I also use Python to build applications
at work!
Found match "Python" ranging from index 11 - 17
Found match "Python" ranging from index 39 - 45

```

```
# illustrating pattern substitution using sub and subn methods
In [544]: re.sub(pattern, 'Java', s2, flags=re.IGNORECASE)
Out[544]: 'I love the Java language. I also use Java to build applications

```

```
          at work!'
In [545]: re.subn(pattern, 'Java', s2, flags=re.IGNORECASE)
Out[545]: ('I love the Java language. I also use Java to build applications

```

at work!', 2)

This concludes our discussion on the various aspects of strings and how they canbe utilized for working with text data. Strings form the basis for processing text, which isan important component in text analytics. The next section briefly discusses some of thepopular text analytics frameworks.

```
이것으로 문자열의 다양한 측면과 텍스트 데이터 작업에 활용할 수있는 방법에 대한 논의를 마칩니다. 문자열은 텍스트 분석의 중요한 구성 요소 인 텍스트 처리의 기초를 형성합니다. 다음 섹션에서는 인기있는 텍스트 분석 프레임 워크에 대해 간략하게 설명합니다.
```



## Text Analytics Frameworks

Like I’ve mentioned before, the Python ecosystem is very diverse and supports a widevariety of libraries, frameworks, and modules in many domains. Because we will beanalyzing textual data and performing various operations on it, you need to knowabout dedicated frameworks and libraries for text analytics that you can just install andstart using—just like any other built-in module in the Python standard library. These frameworks have been built over a long period of time and contain various methods,capabilities, and features for operating on text, getting insights, and making the dataready for further analysis, such as applying machine learning algorithms on pre-processed textual data.

Leveraging these frameworks saves a lot of effort and time that would have beenotherwise spent on writing boilerplate code to handle, process, and manipulate textdata. Thus, the frameworks enable developers and researchers to focus more on solvingactual problems and the necessary logic and algorithms needed for doing so. We havealready seen some of the NLTK library in the first chapter. The following list of librariesand frameworks are some of the most popular text analytics frameworks, and we will beutilizing several of them throughout the course of the book:

```
앞서 언급 한 것처럼 파이썬 생태계는 매우 다양하며 많은 영역에서 다양한 라이브러리, 프레임 워크 및 모듈을 지원합니다. 텍스트 데이터를 분석하고 다양한 작업을 수행하기 때문에 Python 표준 라이브러리에있는 다른 기본 제공 모듈과 마찬가지로 설치하고 사용할 수있는 텍스트 분석을위한 전용 프레임 워크와 라이브러리에 대해 알아야합니다. 이러한 프레임 워크는 오랜 기간 동안 구축되어 텍스트 처리, 통찰력 확보 및 사전 처리 된 텍스트 데이터에 기계 학습 알고리즘을 적용하는 등의 추가 분석을위한 데이터 작성을위한 다양한 방법, 기능 및 기능을 포함합니다.

이러한 프레임 워크를 활용하면 텍스트 데이터를 처리, 처리 및 조작하는 보편적 인 코드 작성에 많은 노력과 시간을 소비하지 않아도됩니다. 따라서 프레임 워크는 개발자와 연구자가 실제 문제를 해결하는 데 더 많은 노력을 기울일 수 있도록하고 필요한 로직과 알고리즘을 수행하는 데 집중합니다. 우리는 이미 첫 번째 장에서 NLTK 라이브러리 중 일부를 보았습니다. 다음 라이브러리 및 프레임 워크 목록은 가장 널리 사용되는 텍스트 분석 프레임 워크 중 일부이며 책의 전체 과정에서 몇 가지를 활용할 것입니다.
```

- NLTK: The Natural Language Toolkit is a complete platformthat contains more than 50 corpora and lexical resources. It alsoprovides the necessary tools, interfaces, and methods to processand analyze text data.

- pattern: The pattern project started out as a research project
  at the Computational Linguistics & Psycholinguistics research
  center at the University of Antwerp. It provides tools and
  interfaces for web mining, information retrieval, NLP, machine
  learning, and network analysis. The pattern.en module contains
  most of the utilities for text analytics.

- gensim: The gensim library has a rich set of capabilities forsemantic analysis, including topic modeling and similarityanalysis. But the best part is that it contains a Python port ofGoogle’s very popular word2vec model (originally available asa C package), a neural network model implemented to learndistributed representations of words where similar words(semantic) occur close to each other.

- textblob: This is another library that provides several capabilitiesincluding text processing, phrase extraction, classification, POStagging, text translation, and sentiment analysis.

- spacy: This is one of the newer libraries, which claims to provideindustrial-strength NLP capabilities by providing the bestimplementation of each technique and algorithm, making NLPtasks efficient in terms of performance and implementation.

  Besides these, there are several other frameworks and libraries that are not dedicatedtowards text analytics but that are useful when you want to use machine learningtechniques on textual data. These include the scikit-learn, numpy, and scipy stack.Besides these, deep learning and tensor-based libraries like theano, tensorflow, andkeras also come in handy if you want to build advanced deep learning models based

  on deep neural nets, convnets, and LSTM-based models. You can install most of theselibrariesusingthepip install <library>commandfromthecommandpromptorterminal. We will talk about any caveats if present in the upcoming chapters when we usethese libraries.

  ```
  - NLTK : Natural Language Toolkit은 50 개가 넘는 보충 자료와 어휘 자원을 포함하는 완전한 플랫폼입니다. 또한 텍스트 데이터를 처리하고 분석하는 데 필요한 도구, 인터페이스 및 메소드를 제공합니다.

  - 패턴 : 패턴 프로젝트가 연구 프로젝트로 시작되었습니다.
    전산 언어학 및 심리 언어학 연구
    앤트워프 대학의 센터. 도구 및
    웹 마이닝, 정보 검색, NLP, 머신 용 인터페이스
    학습 및 네트워크 분석. pattern.en 모듈은 다음을 포함합니다.
    텍스트 분석을위한 대부분의 유틸리티.

  - gensim : gensim 라이브러리에는 주제 모델링 및 유사 분석을 비롯한 대수 분석을위한 풍부한 기능 세트가 있습니다. 그러나 가장 중요한 부분은 유사 단어 (의미 론적)가 서로 가깝게 발생하는 단어의 배분 된 배분을 위해 구현 된 신경망 모델 인 Google의 매우 인기있는 word2vec 모델 (원래 C 패키지로 제공됨)의 Python 포트를 포함한다는 것입니다.

  - textblob : 텍스트 처리, 구문 추출, 분류, POS 태그 지정, 텍스트 번역 및 정서 분석을 비롯한 여러 기능을 제공하는 또 다른 라이브러리입니다.

  - spacy : 이것은 최신 라이브러리 중 하나로서, 각 기술과 알고리즘의 최적 구현을 제공함으로써 산업 강도 NLP 기능을 제공함으로써 NLP 타스크를 성능 및 구현 측면에서 효율적으로 만듭니다.

    이 외에도 텍스트 분석에 전념하지는 않지만 텍스트 데이터에 대한 기계 학습 기술을 사용하려는 경우에 유용한 다른 여러 프레임 워크와 라이브러리가 있습니다. 여기에는 scikit-learn, numpy 및 scipy 스택이 포함됩니다. 이들 외에, theano, tensorflow 및 andkeras와 같은 텐서 기반 라이브러리 및 심층 학습 라이브러리는 고급 딥 학습 모델을 기반으로 구축하려는 경우 유용합니다
    심 신경 그물, convnets 및 LSTM 기반 모델.
  명령 프롬프트에서 <pipeline install> 라이브러리 명령을 사용하여 대부분의 라이브러리를 설치할 수 있습니다. 다음 장에서 라이브러리를 사용할 때주의 사항에 대해 이야기하겠습니다.
  ```

  ​

##Summary

This chapter provides a birds-eye yet detailed view of the entire Python ecosystem andwhat the language offers in terms of capabilities. You read about the origins of the Pythonlanguage and saw how it has evolved overtime. The language has benefits of being opensource, which has resulted in an active developer community constantly striving toimprove the language and add new features. By now, you also know when you should usePython and the drawbacks associated with the language—which every developer shouldkeep in mind while building systems and applications. This chapter also discussed how toset up your own Python environment and deal with multiple virtual environments.

```
이 장에서는 전체적으로 파이썬 생태계와 기능면에서 언어가 제공하는 바를 자세하게 설명합니다. Pythonlanguage의 기원에 대해 읽었을 때, Python 언어가 어떻게 진행되어 왔는지 보았습니다. 이 언어는 opensource라는 이점을 가지고있어서 적극적인 개발자 커뮤니티가 언어를 개선하고 새로운 기능을 추가하기 위해 끊임없이 노력하고 있습니다. 지금까지 여러분은 파이썬을 사용해야하는시기와 언어와 관련된 단점을 알고 있습니다. 모든 개발자는 시스템 및 응용 프로그램을 작성하는 동안이를 염두에 두어야합니다. 또한이 장에서는 자신 만의 Python 환경을 설정하고 여러 가상 환경을 처리하는 방법에 대해서도 설명했습니다.
```

Starting from the very basics, we have taken a deep dive into the various structuresand constructs in the Python language, including data types and controlling code flowusing loops and conditionals. We also explored concepts in various programmingparadigms including OOP and functional programming. Constructs like classes,functions, lambdas, iterators, generators, and comprehensions are tools that will come inhandy in a lot of scenarios when writing quality Python code. You also saw how to workwith text data using the string data type and its various syntaxes, methods, operations,and formats. We also talked about the power of regular expressions and how useful theycan be in pattern matching and substitutions. To conclude our discussion, we looked atvarious popular text analytics frameworks, which are useful in solving problems and tasksdealing with NLP and analyzing and extracting insights from text data.

```
아주 기초부터 시작하여, 우리는 루프와 조건을 사용하여 데이터 유형과 제어 코드 흐름을 포함하여 Python 언어의 다양한 구조와 구조에 대해 자세히 살펴 보았습니다. 우리는 또한 OOP와 함수 프로그래밍을 포함한 다양한 프로그래밍 패러다임에서 개념을 탐구했다. 클래스, 함수, 람다, 이터레이터, 생성자, 이해력 같은 생성자는 양질의 파이썬 코드를 작성할 때 많은 시나리오에서 비합법적 인 도구가 될 것입니다. 또한 문자열 데이터 형식과 다양한 구문, 메서드, 작업 및 형식을 사용하여 텍스트 데이터를 처리하는 방법을 살펴 보았습니다. 우리는 또한 정규 표현식의 힘과 그들이 패턴 매칭과 대체에 얼마나 유용 할 수 있는지에 대해서도 이야기했습니다. 토론을 끝내기 위해 NLP로 문제와 작업을 해결하고 텍스트 데이터에서 통찰력을 분석 및 추출하는 데 유용한 다양한 인기있는 텍스트 분석 프레임 워크를 살펴 보았습니다.
```

This should all get you started with programming in Python. The next chapter buildson the foundations of this chapter as we start to understand, process, and parse text datain usable formats.

```
이것으로 파이썬으로 프로그래밍을 시작할 수 있습니다. 다음 장에서는 텍스트 형식의 유용한 형식을 이해하고 처리하고 파싱하기 시작하면서이 장의 기초를 다룹니다.
```