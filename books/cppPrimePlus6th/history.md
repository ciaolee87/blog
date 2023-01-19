### 23.01.19

* p10. c++ 는 크게 3 파트로 구성되어 있다.
    1. Procedural language from by C
    2. Object-oriented language
    3. Generic programming, supported by C++ templates

* C Complie

~~~ mermaid
stateDiagram

    [*] --> C
    state Specify <<choice>>
    
    C --> Specify
   
    
    Specify --> Compiler1 : Target hardware
    Specify --> Compiler2 : Target hardware
    Specify --> Compiler3 : Target hardware
     
    state Compiler1 {
        [*] --> Preprocessor
        Preprocessor --> ObjectFile : preprocess
        ObjectFile --> Hardware1
        
        state Hardware1 {
            [*] --> Postprocessor
            Postprocessor --> Program : Assembly
            Program --> CPU
            
            note right of Program
                해당 기기에서 실행 가능한 파일
            end note
        }
    }
    
    state Compiler2 {
        [*] --> Process2
        Process2 --> [*]
    }
    
    state Compiler3 {
        [*] --> Process3
        Process3 --> [*]
    }

~~~

* C Philosophy
    * C - Procedural language
    * Go 에서도 비슷한 경향이 있다. Struct 에 method 를 연결하는 방식의 프로그래밍.
      ~~~ mermaid
        stateDiagram-v2
        
        state C {
          Data
          Algorithm
        }
      
      
        state join <<join>>
      
        Data --> join
        Algorithm --> join
      
        join --> Program
        
        Program --> [*]
      
      ~~~

* 단어정리
    * concise: 작은, 간결한 ex) a concise explanation 간결한 설명
    * graft: 이득, 수혜 (무엇인가에서 물려받은, 이어받은)
    * tangle: (머리카락 등 방해물) 엉키다, 잡다, 방해하다, 빠트리다
        * Her hair was tangled with weeds.
        * get tangled up with some wild associates
        * tangle oneself in one's own snare (자업자득)
    * correspond : cor + respond = 서로 답하다.
    * whereas: 접속사 - ~에 비하면
    * thus : 접속사 - 앞서 말한바와 같이
    * apparent: 【ap(…의 눈앞에)＋pare(나타나다)＋ent(상태로)】 확실히 보이는, 식별할수있는
    * 