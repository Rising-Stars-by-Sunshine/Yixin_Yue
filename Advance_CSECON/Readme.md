**Question1: Analyze your experience with oTree, identifying pain points in behavioral game theory research. Review related literature and class discussions to understand experimental economics' goals. Propose a software solution that outperforms oTree in at least three aspects, enhancing strategic interaction studies. Highlight why these advancements are crucial. Submit a concise essay question answer (500 words max) with your analysis and proposals, backed by literature and class insights. Your innovative ideas can significantly contribute to experimental economics, addressing current limitations and paving the way for advanced research methodologies.**

Based on my personal experience, I think:
- the entire deployment process is too complicated for researchers who are unfamiliar with Python programming or web development concepts. People need to switch back and forth between different platforms to finish the deployment process. Although oTree offers many documentation and resources, there is still a coding requirement for customizing the game, which may consume a lot of time for the user to understand the internal logic.
- Additionally, the limited visual design options in oTree's default interface are not very visually engaging, the playing page is a little bit hard to operate because there are three windows open on a web page. I have to drag it up and down repeatedly to play and see the results.
- Debugging experiments in oTree can also be complex, especially for researchers who are not familiar with programming concepts or debugging tools. The error messages, while technically accurate, are not easily understandable for typical users as well. Therefore, users may struggle to comprehend what went wrong or how to address the issue based on the information provided in the error message.

To advance oTree based on the points I mentioned above, using built-in functions to reduce the programming complexity is crucial. In particular, introducing PlanOut language can potentially fix that. According to Bakshy, Eckles, and Bernstein (2014), PlanOut separates experimental design from application code in online field experiments by allowing experimenters to concisely describe experimental designs using a specific language. This separation can help users focus on defining how units are randomly assigned to conditions based on parameters, rather than embedding experimental logic within the application code. By encapsulating experimental logic in simple scripts that assign values to parameters, PlanOut provides a clear and structured way to define and manage experiments. Additionally, integrating more advanced and intuitive interface design tools like Figma can enhance the visual appeal of experimental interfaces. Implement interactive debugging tools within the oTree interface to assist users in diagnosing and resolving errors in real time. This could include features such as code highlighting, variable inspection, and error visualization to aid users in identifying issues within their experiments. These enhancements have the potential to significantly enhance the user experience for researchers with basic coding skills, enabling them to swiftly set up and customize their experiments with minimal effort. 
![WeChatfaee0cdd9c06f4c950d4b55e42b30c84](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/7b3c665c-edc1-47ff-b335-cf4b5c74e9fa)


**Question2: Delve into the limitations of current multi-agent reinforcement learning (MARL) frameworks, focusing on environment constraints and agent algorithm customizations. Choose a classic game (e.g., Prisoner's Dilemma, Battle of the Sexes, or the Trust Game) to illustrate these limitations. Describe the development process of a MARL agent for your selected game, detailing the definition of states, actions, and rewards grounded in fundamental behavioral assumptions. Your analysis should provide insights into overcoming MARL's current limitations, fostering advancements in the field. Submit a comprehensive report (500 words max) with your findings and proposals.**

The development process of a Multi-Agent Reinforcement Learning (MARL) agent for Connect Four in the petting zoo environment involves several key steps. Firstly, the state space is defined based on the current configuration of the Connect Four board, including the positions of the tokens played by both players and additional features like the current player's turn and potential winning configurations. Next, the action space is defined, representing the possible moves the agent can make, typically involving dropping a token into one of the columns on the board. Actions are limited to valid moves only, i.e., columns that are not already full. Subsequently, set the reward to incentivize desirable behavior and discourage undesirable behavior, assigning positive rewards for winning the game, strategic moves, and progress towards a winning configuration, and vice versa. Finally, the agent's behavior is grounded in fundamental behavioral assumptions such as rationality, learning, and adaptation.

![21921712582532_ pic](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/b2dce350-bd36-48cc-a4c9-bc796ebde10d)

This MARL did a good job of understanding the rules of Connect Four, however, its ability to simulate human decision-making, particularly strategic thinking aimed at swiftly winning the game, is still not mature enough. For instance, a human player would prioritize placing a white token to block a potential win by the black player in the first row. In such a scenario, human reasoning would prioritize strategic moves to thwart the opponent's progress, a capability not fully mirrored in the agent's behavior. To improve, I think the program can achieve superhuman performance in these strategic games by reinforcement learning from self-play just like AlphaGo(Silver et al. 2018). 

**Question3: Brainstorm your research idea by criticizing existing research: Critiquing and Expanding upon Existing Research**

**Research question:** How to design a practical incentive mechanism for Federated Learning with partial client participation, to ensure convergence to a globally optimal unbiased model? 

**Methodology:** proposes a game-theoretic incentive mechanism for Federated Learning (FL) with randomized client participation. The server adopts a customized pricing strategy to motivate various clients to participate in FL with different probabilities. Each client is involved in this process by responding to the server's monetary incentive and selecting its participation level. 

**Application Scenarios:** Federated Learning systems where multiple clients collaborate to train a global model with a limited budget while keeping their data decentralized and private. 

**Critique of the Research Question:** This research question is important since it addresses key challenges in Federated Learning by proposing a new incentive mechanism considering clients' intrinsic values. It marches into the intersection of computer science and economics. By designing a flexible pricing mechanism, this framework can improve global model performance with the best budget allocation. 

**Critique of the Methodology:** The methodology seems rational to me for its reliance on empirical data from real datasets and implementation on a hardware prototype. Initially, I questioned how to guarantee the system's resilience against false reports of user participation level. Professor Luo explained that they developed an additional mechanism to incentivize truthfulness, ensuring that honesty is the optimal choice for users, or else they risk giving the money back. 

**Critique of the Application Scenario:** I think it requires further experimental validation and real-world deployment of the proposed mechanism in FL systems. Additionally, exploring the scalability of the approach to larger datasets and more complex models could be a valuable direction for future research. 

**Beyond Computer Science and Economics:** My question for Chatgpt: Do you think the incentivized framework will still work considering the bounded rationality of both human and AI agents? What if the client is replaced by an AI agent?

Response from ChatGPT:
![21931712582684_ pic](https://github.com/Rising-Stars-by-Sunshine/Yixin_Yue/assets/164857136/fed47a12-f71b-419e-8d1b-8783cb89c9b2)

**Bibliography:**

Bakshy, Eytan, Dean Eckles, and Michael S. Bernstein. 2014. "Designing and Deploying Online Field Experiments." Proceedings of the 23rd International Conference on World Wide Web, April. https://doi.org/10.1145/2566486.2567967. 

Silver, David, Thomas Hubert, Julian Schrittwieser, Ioannis Antonoglou, Matthew Lai, Arthur Guez, Marc Lanctot, et al. 2018. "A General Reinforcement Learning Algorithm That Masters Chess, Shogi, and Go through Self-Play." Science 362 (6419): 1140–44. https://doi.org/10.1126/science.aar6404. 

Luo, Bing, Yutong Feng, Shiqiang Wang, Jianwei Huang, and Leandros Tassiulas. "Incentive Mechanism Design for Unbiased Federated Learning with Randomized Client Participation." In 2023 IEEE 43rd International Conference on Distributed Computing Systems (ICDCS), pp. 545-555. IEEE, 2023.





