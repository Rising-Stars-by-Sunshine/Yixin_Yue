**Question1: Analyze your experience with oTree, identifying pain points in behavioral game theory research. Review related literature and class discussions to understand experimental economics' goals. Propose a software solution that outperforms oTree in at least three aspects, enhancing strategic interaction studies. Highlight why these advancements are crucial. Submit a concise essay question answer (500 words max) with your analysis and proposals, backed by literature and class insights. Your innovative ideas can significantly contribute to experimental economics, addressing current limitations and paving the way for advanced research methodologies.**

Based on my personal experience, I think:
- The whole deployment process might be a little bit complicated for researchers who are unfamiliar with Python programming or web development concepts. People need to switch back and forth between different platforms(oTree-game set up, Desktop-store folder, VSC-control terminal, Web browser-open) to finish the deployment process. Although oTree offers many documentation and resources, there is still a coding requirement for customizing the game, which may take additional time for the user to understand the internal logic.
- The limited interface design options in oTree's default interface are not very visually engaging, the playing page is a little bit hard to operate because there are three windows open on a web page **(see fig.1)**. I have to drag it up and down repeatedly to play and see the data. I think it might be better if people can play in a pop out window.
- There is a potential issue about data privacy. Since oTree experiments are typically hosted on servers of researchers or institutions, there may cause data exposure if the servers are not adequately secured.
![21951712587939_ pic](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/e0453c81-2b93-4166-9616-220c92728a43)

*fig.1. Screenshot of the crowded window*


To advance oTree based on the points I mentioned above, **see fig.2.**
- Using built-in functions to reduce the programming complexity is crucial. In particular, introducing PlanOut language can potentially fix that. According to Bakshy, Eckles, and Bernstein (2014), PlanOut separates experimental design from application code in online field experiments by allowing experimenters to concisely describe experimental designs using a specific language. This separation can help users focus on defining how units are randomly assigned to conditions based on parameters, rather than embedding experimental logic within the application code. By encapsulating experimental logic in simple scripts that assign values to parameters, PlanOut provides a clear and structured way to define and manage experiments.
- Additionally, integrating more intuitive interface design tools can help the researchers enhance the visual appeal of experimental interfaces.
- More security measures should be done to protect participants' data from unauthorized access or breaches. When transferring data between oTree servers and external systems, researchers must use secure protocols (e.g., HTTPS) to encrypt data in transit and prevent interception or tampering. Using oTree development should comply with applicable data protection laws and regulations, such as the General Data Protection Regulation (GDPR) or the Health Insurance Portability and Accountability Act (HIPAA) in the US.
![21941712587909_ pic](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/7bd0c2b9-2877-4d53-aa40-1e8e69aa05ad)

*fig.2. Mindmap for Upgrade oTree*



**Question2: Delve into the limitations of current multi-agent reinforcement learning (MARL) frameworks, focusing on environment constraints and agent algorithm customizations. Choose a classic game (e.g., Prisoner's Dilemma, Battle of the Sexes, or the Trust Game) to illustrate these limitations. Describe the development process of a MARL agent for your selected game, detailing the definition of states, actions, and rewards grounded in fundamental behavioral assumptions. Your analysis should provide insights into overcoming MARL's current limitations, fostering advancements in the field. Submit a comprehensive report (500 words max) with your findings and proposals.**
Implementation for Trust Game:

https://colab.research.google.com/drive/1pL-qFpME7lY4BFtGiFkTnLVdYjCH-dCL?usp=sharing

![21991712636751_ pic](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/9a858e4a-5c05-4ce5-bd6e-84289022d7c3)

*fig.3. Mindmap of the environment components.*

I think the Trust Game environment **(fig.3)** for MARL has several limitations. 
- It has only two agents and limited actions (SEND or RECEIVE), coupled with a fixed game length, restricts its applicability to capturing the complexity of real-world interactions **(fig.4)**.(as the number of agents increases, the environment becomes less stable, and coordination among agents becomes more difficult.)

![22001712637506_ pic](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/1514ecd4-672d-4c8a-90c4-a0a6f0835628)

*fig.4. Screenshot of playing Trust Game*

- The lack of comprehensive state information and a limited action space may hinder agents' ability to find the optimal strategies. Deterministic rewards further simplify the learning process but fail to capture the uncertainty present in real-world environments. Furthermore, the fixed roles assigned to agents and the absence of a learning mechanism limit the environment's ability to explore dynamic agent interactions and emergent behavior.

To address:
- Expand the environment to include more agents, a broader range of actions and states. Allow mutation/inheritance or
competition between two types in a finite population.

- Use more sophisticated learning methods, such as Frequency-Adjusted Q-learning(Shi and Rong 2022), Grey Wolf Optimization and Neural Networks(Emary, Zawbaa, and Grosan 2018) to learn the evolutionary dynamics in this system.

**Question3: Brainstorm your research idea by criticizing existing research: Critiquing and Expanding upon Existing Research**

**Research question:** How to design a practical incentive mechanism for Federated Learning with partial client participation, to ensure convergence to a globally optimal unbiased model? (Luo et al., 2023)

**Methodology:** proposes a game-theoretic incentive mechanism for Federated Learning (FL) with randomized client participation. The server adopts a customized pricing strategy to motivate various clients to participate in FL with different probabilities. Each client is involved in this process by responding to the server's monetary incentive and selecting its participation level. 

**Application Scenarios:** Federated Learning systems where multiple clients collaborate to train a global model with a limited budget while keeping their data decentralized and private. 

**Critique of the Research Question:** This research question is important since it addresses key challenges in Federated Learning by proposing a new incentive mechanism considering clients' intrinsic values. It marches into the intersection of computer science and economics. By designing a flexible pricing mechanism, this framework can improve global model performance with the best budget allocation. 

**Critique of the Methodology:** The methodology seems rational to me for its reliance on empirical data from real datasets and implementation on a hardware prototype. Initially, I questioned how to guarantee the system's resilience against false reports of user participation level. Professor Luo explained that they developed an additional mechanism to incentivize truthfulness, ensuring that honesty is the optimal choice for users, or else they risk giving the money back. 

**Critique of the Application Scenario:** I think it requires further experimental validation and real-world deployment of the proposed mechanism in FL systems. Additionally, exploring the scalability of the approach to larger datasets and more complex models could be a valuable direction for future research. 

**Beyond Computer Science and Economics:** 
My question for Chatgpt 3.5:

Do you think it is feasible to introduce such incentive mechanism to Federated learning to achieve an unbiased and high-performance global model considering bounded rationality of AI and Human agents

Response from ChatGPT **(fig.5)**:

![22011712638023_ pic](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/39d65de1-8470-4735-8bd0-869c8e390100)

*fig.5. a screenshot of response from chatgpt*

In general, Chatgpt admitted that implementing such a mechanism within existing FL frameworks is feasible from a technical perspective, , but it entails complexities in algorithm design to adapt to varying levels of participation and data relevance. While computational resources may be required for tracking participant contributions and managing incentive distributions, so there is a need to advance distributed computing and blockchain technologies to mitigate these challenges. 


**Bibliography:**

Bakshy, Eytan, Dean Eckles, and Michael S. Bernstein. 2014. "Designing and Deploying Online Field Experiments." Proceedings of the 23rd International Conference on World Wide Web, April. https://doi.org/10.1145/2566486.2567967. 

Emary, E., Hossam M. Zawbaa, and Crina Grosan. 2018. “Experienced Gray Wolf Optimization through Reinforcement Learning and Neural Networks.” IEEE Transactions on Neural Networks and Learning Systems 29 (3): 681–94. https://doi.org/10.1109/tnnls.2016.2634548.

Shi, Yiming, and Zhihai Rong. 2022. “Analysis of Q-Learning like Algorithms through Evolutionary Game Dynamics.” IEEE Transactions on Circuits and Systems II: Express Briefs 69 (5): 2463–67. https://doi.org/10.1109/tcsii.2022.3161655.

Luo, Bing, Yutong Feng, Shiqiang Wang, Jianwei Huang, and Leandros Tassiulas. 2023. “Incentive Mechanism Design for Unbiased Federated Learning with Randomized Client Participation.” ArXiv (Cornell University), April. https://doi.org/10.48550/arxiv.2304.07981.





