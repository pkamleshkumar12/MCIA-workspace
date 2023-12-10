# 2. Identifying Anypoint Platform components and Capabilities

![Untitled](2%20Identifying%20Anypoint%20Platform%20components%20and%20Cap%20b689c8d17bfa43e6867556f409633008/Untitled.png)

- **Control Plane**
    - The components of the Anypoint Platform that are involved in the design, deployment, and management of APIs and Mule applications.
- **Runtime Plane**
    - The  component of the Anypoint Platform where the APIs and Mule applications are deployed
    
- A **Mule application** consists of code and related files, and it runs in a Mule runtime
    - **Deployed** or packaged as a JAR
    - **Triggered** by internal or external **events**
    - **Processes** each event through the **event processors** and **connector operations**
    
    ![Untitled](2%20Identifying%20Anypoint%20Platform%20components%20and%20Cap%20b689c8d17bfa43e6867556f409633008/Untitled%201.png)
    
- Mule applications are deployed to a Mule runtime
    - A lightweight, Java-based integration platform or application server
    - Provisioning options: CloudHub, Runtime Fabric on Openshift, Runtime Fabric on Self-Managed Kubernetes, Runtime Fabric on VMs/ Bare Metal, and customer-hosted
    - Studio comes with an embedded Mule runtime for local development
    
- Mule applications accept and process **events (** which are created via an event source) through a series of **event processors** that are linked together in one or more **********flows**********
- A **********flow********** is a linked sequence of event processors
    - Think of each event processor as a Lego block and a flow as something you construct by linking the blocks together in a certain order
    - Must have at least one event processor
    - Can be invoked by a flow reference
    - Error handling and event sources are optional

![Untitled](2%20Identifying%20Anypoint%20Platform%20components%20and%20Cap%20b689c8d17bfa43e6867556f409633008/Untitled%202.png)

- A flow can start with an ************************event source************************
    - Event source accepts inbound events and converts them to **********************Mule events**********************
    - The Mule event is passed or copied between event processors in the flow
    
    ![Untitled](2%20Identifying%20Anypoint%20Platform%20components%20and%20Cap%20b689c8d17bfa43e6867556f409633008/Untitled%203.png)
    
    ## An API-led approach using the Anypoint Platform
    
    - At first, **Component interfaces** can be designed with **API Specification** that is easier for less technical stakeholders to understand
        - Write, publish, and version APIs in **Anypoint Design Center**
        - Share, mock, test, and reuse APIs with **Anypoint Exchange**
        - **********Test********** and ******mock******  APIs in Anypoint Exchange using an API portal and its ************************API Console************************ UI
        - Encourages visibility and early agreement by less technical stakeholders.
    
    ### Advantages of developing with published APIs
    
    - ********Building validation********  and ************************************field constraints************************************  are specified in the API
        - Developers do not have to code these validation checks or error types, speeding up API implementation and development
        - Standard errors are automatically generated
    - APIs encourage ****************************early testing****************************  and  ******************************self-discovery******************************
        - API clients can be tested and “fail fast” before API implementations are created
            - Promotes parallel development and self-discovery of existing services and other reusable assets
        - Complex business objects and constraints are specified and agreed upon in the API specifications