# 结题时间

**校级普通项目**结题时间为2025年6月

**校级重点项目**项目结题时间为2025年9月

# 验收材料

1. 课外开放实验校级重点项目结题报告（在系统中提交电子版）；
2. 项目实验报告（在系统中提交电子版）
3. 实验过程三幅照片原文件及图片说明
4. 软件源程序（在系统中提交电子版）
5. 源于**校级重点项目**开放实验的标志性成果影印件电子文档，或证明材料（在系统中提交电子版）

# IDEA


## CNN+SVM+MBTI+Flow+PT→？


* CNN表情识别[link1](https://www.kaggle.com/code/naeemahmedhaji/facial-expression-recognition-using-cnn)and[link2](https://www.kaggle.com/code/mohammedabdeldayem/facial-expression-recognition)
* 使用[PyQT](https://www.kaggle.com/code/mohammedabdeldayem/facial-expression-recognition)构建客户端，导入训练好的大模型[link](https://zhuanlan.zhihu.com/p/274436031)
* MBTI：各不同的MBTI得分对表情收集的加权
* [Flow](https://en.wikipedia.org/wiki/Flow_(psychology))：使用SVM或者LLM对用户状态进行分析（或者某种程度上的假实现）
* PT：[番茄工作法Pomodoro Technique](../杂记/番茄工作法Pomodoro%20Technique.md)

工作或者学习等场景下的辅助系统

* 目的是为了帮助用户快速进入心流状态提高学习工作效率。
* 项目实施：使用CNN训练模型，配合硬件实现表情识别的功能；用户填写的MBTI问卷生成对应的多个数值，利用问卷的结果与之前识别的表情相结合，使用支持向量机或LLM模型，实时判断用户的心理状态，然后给用户一个及时的反馈，帮助用户回到一个高效的学习或工作状态。
* 用户的使用流程：第一次使用填写问卷，使用前安排一段时间的任务，然后软件就是自动的给用户提供建议。

# 标题

1. 基于CNN表情分析与LLM情感解读的个性化互动优化系统
2. 基于CNN-SVM心流状态检测与引导系统
3. 基于卷积神经网络与支持向量机的心流状态检测引导系统


# 特点

1. 多模态数据融合：
 * 面部表情识别（CNN）： 通过CNN模型分析用户的面部表情，提取出与心流状态高度相关的特征，如微笑、皱眉、眼睛睁开程度等。
 * MBTI人格类型： 结合MBTI人格类型，可以更深入地理解不同个体进入心流状态的特征。例如，INTJ型人格可能更倾向于在高度抽象的任务中进入心流。
 * 语言模型（LLM）： 通过分析用户在使用软件时的语言表达，如用词、句式、情感倾向等，进一步捕捉用户的心流状态。
4. 心流状态的定义与特征提取：
 * 明确心流状态的定义： 结合心理学研究，明确定义心流状态的核心特征，如高度专注、时间扭曲、自我意识消失等。
 * 特征提取： 基于以上定义，提取与心流状态相关的关键特征，并设计相应的算法进行检测。
5. 检测模型的构建：
 * 多模态融合模型： 构建一个能够融合CNN、MBTI和LLM输出的模型，以提高检测的准确性。
 * 机器学习算法： 可以采用随机森林、支持向量机、神经网络等机器学习算法进行训练和预测。
6. 心流状态的引导：
 * 个性化反馈： 根据检测结果，为用户提供个性化的反馈，如“您现在非常专注，保持下去！”、“您似乎有些分心，尝试调整任务难度”。
 * 任务调整： 根据用户的MBTI类型和当前状态，动态调整任务的难度、复杂度和反馈方式，引导用户进入心流状态。
 * 环境优化： 提供一些环境优化建议，如调整背景音乐、光照等，以营造更利于心流产生的氛围。



 * 关键词： 心流、面部表情识别、MBTI、自然语言处理、机器学习、个性化推荐
 * 潜在研究方向：
   * 多模态情感识别： 探讨如何将生理信号、面部表情和文本数据融合，以更准确地识别情感状态。
   * 个性化心流干预： 研究如何根据个体差异，设计个性化的心流干预策略。
   * 心流与学习： 探讨心流状态对学习效果的影响，以及如何通过技术手段促进学习者进入心流状态。

建议您在Google Scholar上搜索以下关键词组合，以获取更详细的论文信息：
 * "flow state" AND "facial expression recognition" AND "MBTI"
 * "personalized learning" AND "flow theory" AND "machine learning"
 * "multimodal emotion recognition" AND "心流"

# 相关文章

#### 破译可见性和交互性对 AI 驱动型网站中网站氛围和客户粘性的技术贡献：在线流状态的关键功能

[Deciphering technological contributions of visibility and interactivity to website atmospheric and customer stickiness in AI-driven websites: The pivotal function of online flow state](https://www.sciencedirect.com/science/article/abs/pii/S0969698924000912)

> [!心流体验的概述]+
> Flow theory encapsulates a psychological state where individuals are profoundly immersed and attentively fixated on a task, yielding an amplified sense of euphoria and fulfillment (Brailovskaia and Margraf, 2024; Uhm et al., 2023; Zhao et al., 2024). This stage is characterized by an all-encompassing absorption in the undertaken activity, during which temporal perception may appear to decelerate or even halt. In this apogee of flow, individuals' perceptual acuity towards peripheral stimuli becomes markedly attenuated; extraneous stimuli are methodically excluded, sharpening focus on the task at hand. Concurrently, there is a notable attenuation in self-awareness; individuals respond solely to immediate objectives and feedback, experiencing a heightened sense of dominion over their environment. Flow theory elucidates the intricate nexus between profound concentration and the ensuing sensations of exhilaration and gratification (Zhang et al., 2023). Within the flow state, the perception of external stimuli is curtailed, and self-consciousness subtly recedes into the background. This phenomenon could manifest in diverse activities, ranging from athletic endeavors, literary engagement, to cinematic experiences. Particularly, within computer-mediated contexts, this gives rise to the concept of online flow. Hofmann et al., have extended Csikszentmihalyi's flow theory to encompass computer-mediated environments (Hofmann et al., 2024). They posit that the state of online flow can be achieved during intense engagement in digital activities. Flow, in this context, refers to the emotive responses of computer users towards digital interactions, where enjoyment and exploration are fundamental to human-computer interplay. Flow has been identified as a pivotal element in various online behaviors, including web browsing, online gaming, software utilization, and e-commerce engagements (Khare et al., 2023; Rohit et al., 2024).





























