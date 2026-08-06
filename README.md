flowchart LR
    subgraph LAN["Local Area Network (MAC Layer)"]
        A[💻 Laptop] 
        B[🖥️ Desktop] 
        C[🖨️ Printer] 
        S["🔌 Switch"]
        A --> S
        B --> S
        C --> S
    end

    subgraph WAN["Internet Border (IP Layer)"]
        R["🌐 Router"]
        I["☁️ Internet"]
        S == MAC Addresses ==> R
        R == IP Addresses ==> I
    end

    classDef device fill:#2d3748,stroke:#4a5568,color:#fff;
    classDef switch fill:#1a365d,stroke:#2b6cb0,color:#fff;
    classDef router fill:#742a2a,stroke:#9b2c2c,color:#fff;
    
    class A,B,C,I device;
    class S switch;
    class R router;
