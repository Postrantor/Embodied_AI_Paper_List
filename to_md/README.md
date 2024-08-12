---
> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [mp.weixin.qq.com](https://mp.weixin.qq.com/s/T-PeVzdJ_mJra0sUynYZqg)
---

在人工智能领域的快速发展中，**具身智能**正迅速成为一个备受关注的研究方向。具身智能不仅仅局限于解决虚拟环境中的抽象问题，更强调智能体与现实世界的交互能力。**它被视为实现通用人工智能的重要途径，其核心在于智能体能够在数字空间和物理世界中灵活应对复杂多变的环境。**

近年来，多模态大模型和机器人技术的快速发展为具身智能研究带来了新的机遇。然而，**目前学术界缺乏一个全面系统的具身智能研究现状梳理。**为填补这一空白，鹏城实验室多智能体与具身智能研究所联合中山大学 HCP 实验室的研究人员对**近 400 篇相关文献**进行了深入调研**，推出了多模态大模型时代的全球首篇具身智能综述。。**

这项研究首先介绍了具有代表性的具身机器人和具身仿真平台，深入分析了其研究重点和局限性。随后，研究团队从四个核心方面深入探讨了具身智能的研究内容：具身感知、具身交互、具身智能体以及虚拟到现实的迁移。**这些方面涵盖了当前最前沿的方法、基本范式和全面的数据集。**

**![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBCcjRxJOjagW2HTo17FibwVJd12Nbya40WJmYhmK9kckroNTaMfzmZQg/640?wx_fmt=other&from=appmsg&tp=webp&wxfrom=13&wx_lazy=1&wx_co=1)**

- 论文地址: https://arxiv.org/pdf/2407.06886
- 具身智能 Paper List:

  https://github.com/HCPLab-SYSU/Embodied_AI_Paper_List

## **具身智能的历史发展**

**具身智能的概念可以追溯到 1950 年艾伦 • 图灵提出的具身图灵测试。**这一概念旨在评估智能体是否具备在物理世界中应对复杂性和不确定性的能力，而不仅仅是解决虚拟环境中的抽象问题。图灵的这一思想为后续的人工智能研究提供了重要的理论基础。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBaMk3zqOaNWkCTYBpDJRRchl4E36GibJYMWKxPhaFiacJI7xoUq5cAXpw/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_具身智能体框架_

随着时间的推移，具身智能逐渐发展成为一个跨学科领域，涉及计算机视觉、自然语言处理和机器人技术等多个关键技术。**这种跨学科的特性使得具身智能能够整合不同领域的先进技术，为解决复杂的实际问题提供了\*\***新的可能性。\*\*

在具身任务中，智能体需要理解人类指令中的意图，主动探索环境，感知来自虚拟和物理世界的多模态信息，并执行相应的操作以完成复杂任务。这种多方面的能力要求使得具身智能成为了实现通用人工智能的重要途径之一。

近期多模态模型的进展显示出了在复杂环境中比传统深度强化学习方法**更强的多样性、灵活性和泛化能力**。这些进展为具身智能的发展提供了新的技术支持，使得智能体能够更好地理解和应对复杂的环境。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBicibx2MfDR4jQ1g9pWrjGIkTLrgkQ3KlNSEYODTFy7YiaxTBo7sMto1Kw/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_本综述整体架构_

## **具身机器人类型及应用**

具身机器人是具身智能在物理世界中的重要载体。根据应用场景的不同，具身机器人可以分为多种类型，每种类型都有其特定的优势和应用领域:

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBkXTdhlPxDyqqcqmVINuEdR99XTUU2auiav7QicSiaCFeOLpQaDGY4nWxw/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_不同形态的具身机器人_

**基座型机器人**

固定基座型机器人，如机械臂，常用于实验室自动化、教育和工业领域。这类机器人通常具有高精度和重复性，适合执行需要精确控制的任务。

**轮式机器人**

轮式机器人因其高效的机动性而广泛应用于物流、仓储和安全检查。它们能够在平坦的地面上快速移动，适合在室内或结构化环境中执行任务。

**履带机器人**

履带机器人具有强大的越野能力，适用于农业、建筑和灾难应对。这类机器人能够在复杂的地形上行走，是野外作业和极端环境探索的理想选择。

**四足机器人**

四足机器人以其稳定性和适应性著称，适合复杂地形的探测和救援任务。它们能够模仿动物的行走方式，在不平坦的地形上保持平衡和稳定性。

**人形机器人**

人形机器人凭借灵巧的手部操作能力，在服务业、医疗保健等领域展现出广阔前景。这类机器人的设计旨在模仿人类的外形和动作，使其能够更自然地与人类互动和在人类环境中工作。

**仿生机器人**

仿生机器人通过模仿自然生物的运动方式，能够在复杂动态环境中执行特定任务。这类机器人的设计灵感来自于自然界中的生物，如蛇形机器人、鱼形机器人等，能够适应特殊的环境和任务需求。

## **具身智能仿真平台**

具身智能仿真平台在研究中扮演着重要角色。这些平台提供了成本效益高、安全可控的实验环境，支持快速原型设计，并为更广泛的研究群体提供了便利。仿真平台还可以生成用于训练和评估的数据，为算法比较提供标准化基准。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBkYwY6ibROA5valKUuD2MMlBdVs2Bia4c8aibkMjruR9PsPmBzrcuHeA3Q/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_通用仿真平台_

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBHt8t9jAmWsxC9hejNRLLoT1HOgK5BGE34Dic4XnwMZkovuib2ibYtPo5g/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_基于真实场景的仿真平台_

**基于底层仿真的通用平台**  
这类平台提供了一个通用的仿真环境，可以模拟各种物理场景和机器人类型。它们通常包含物理引擎，能够模拟真实世界的物理特性，如重力、摩擦等。这些平台适合进行广泛的机器人学习和控制实验。

**基于真实场景的仿真平台**  
这类平台专注于模拟特定的真实世界场景，如家庭环境、办公室或户外场景。它们通常提供更高的视觉真实性和场景复杂度，适合研究具身智能在特定应用场景中的表现。

这些仿真平台在构建逼真的模拟环境方面发挥着关键作用，需要考虑环境的物理特性、对象属性及其相互作用。高质量的仿真对于缩小仿真到现实的差距至关重要，能够提高在真实世界中部署的具身智能系统的性能。

## **具身感知**

具身感知是具身智能的核心能力之一。与传统的图像识别不同，具有具身感知能力的智能体需要在物理世界中移动并与环境互动，这要求对三维空间和动态环境有更深入的理解。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBlFqWDodMBxfaMH5oiaNoa3oxJQ47D0gwriaUhIiaOpCzExsr5KFvW2YLQ/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_主动视觉感知框架_

**主动视觉感知**

主动视觉感知指智能体能够主动控制其感知器官 (如摄像头) 以获取最有用的信息。这包括视角选择、注意力机制和主动探索策略。通过主动视觉感知，智能体可以更有效地收集环境信息，提高任务执行效率。

**3D 视觉定位**

3D 视觉定位涉及智能体在三维空间中确定自身位置和周围物体位置的能力。这对于导航、物体操作和空间推理至关重要。最新的视觉编码器预训练技术提供了对物体类别、姿态和几何形状的精确估计, 使具身模型能够全面感知复杂动态环境。

**视觉语言导航**

视觉语言导航任务要求智能体根据自然语言指令在视觉环境中导航。这需要智能体能够理解语言指令，将其与视觉观察相结合，并规划相应的导航路径。强大的大语言模型极大地提升了机器人理解人类语言指令的能力，并为具身机器人对齐视觉和语言表示提供了可行方法。

**非视觉感知**  
除视觉外，其他感知模态如触觉、听觉等也在具身感知中扮演重要角色。例如，触觉传感可以帮助机器人感知物体的质地、重量和形状，这对于精确的物体操作至关重要。多模态感知的整合是提高具身智能体环境理解能力的关键。

## **具身交互**

具身交互是指智能体在物理或模拟空间中与人类和环境进行互动的能力。这种能力对于实现真正的智能交互至关重要。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBw7V5jvsfrT423HzBFn1u9VVianhZZdMrUP5ibDRlAhmRZGkp9JfFxYAA/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_具身问答框架_

**具身问答**  
具身问答任务要求智能体从第一人称视角探索环境，收集回答问题所需的信息。这不仅需要智能体具备自主探索和决策能力，还要判断何时停止探索以回答问题。具身问答任务考验了智能体的环境理解、信息整合和语言生成能力。

**具身抓取**  
具身抓取涉及基于人类指令执行物体操作，需要全面的语义理解、场景感知、决策和稳健的控制规划。最新的研究将传统的机器人运动学抓取与大型模型 (如大语言模型和视觉语言基础模型) 相结合，使智能体能够在多感官感知下执行复杂的抓取任务。这种结合提高了具身智能体执行复杂任务的能力，使其能够更灵活地应对各种抓取场景。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITB53YoRQ0gTMmtOhjLH8gzM0QozMYK5DHk4SA5bvqIv7GoRCnGNla9Lg/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_语言引导的交互式抓取框架_

## **具身智能体**

具身智能体是能够感知环境并采取行动以实现特定目标的自主实体。多模态大模型的进**展进一步扩大了智能体在实际场景中的应用范围。**

**高层次具身任务规划**  
高层次具身任务规划涉及将抽象复杂的任务分解为具体的子任务。这需要智能体具备强大的推理能力，能够理解任务的整体目标，并制定合适的策略来实现这些目标。高层次规划通常涉及长期目标设定、任务分解和优先级排序。

**低层次具身行动规划**  
低层次具身行动规划关注如何通过有效利用具身感知和交互模型，或利用基础模型的策略功能，逐步实施子任务。这包括运动规划、轨迹生成和实时控制等方面。低层次规划需要考虑环境的物理约束和智能体自身的运动能力。

**多模态感知和交互**  
为了在信息丰富且复杂的现实世界中运行，具身智能体已经发展出强大的多模态感知、交互和规划能力。这包括视觉、听觉、触觉等多种感知模态的，以及与环境和人类的多种交互方式。多模态能力使得智能体能够更全面地理解环境，做出更合理的决策。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBVNOOEwW7PO9AEUOrh5sSKz6DC77TCmkupn2icoYvz550PFSUicu60tjw/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_基于多模态大模型的具身智能体框架_

**## \*\*\*\***虚拟到现实的迁移\*\*\*\*

虚拟到现实的迁移 (Sim-to-Real adaptation) 是具身智能研究中的一个重要课题，指的是将模拟环境 (数字空间) 中学习到的能力或行为转移到现实世界 (物理世界) 中的过程。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/KmXPKA19gWibdMk4VdRJ9yicibyx9icPmITBqX1UW1bJtRM9U5nicv5P5EPtws5bcFe0kGDT9IW8JaqY9pZMn2nQmwg/640?wx_fmt=other&from=appmsg&wxfrom=5&wx_lazy=1&wx_co=1&tp=webp)

_五种虚拟到现实的迁移方案_

**具身世界模型**  
具身世界模型是智能体对环境的内部表示，包括对物理规律、物体属性和环境动态的理解。高质量的世界模型可以帮助智能体更好地预测环境变化，从而在现实世界中做出更准确的决策。

**数据收集与训练方法**  
有效的数据收集和训练方法对于缩小仿真和现实之间的差距至关重要。这包括使用领域随机化技术增加仿真数据的多样性，以及利用真实世界数据进行微调或迁移学习。

**具身控制算法**  
具身控制算法需要能够适应仿真和现实之间的差异。这可能涉及鲁棒控制方法、自适应控制策略或基于模型的强化学习技术。

**Sim-to-Real 范式**  
研究团队介绍了五种不同的 Sim-to-Real 范式, 为这一领域的研究提供了系统的指导:

直接迁移: 直接将在仿真中训练的模型应用于现实环境。

领域随机化: 在训练过程中引入随机性, 增强模型的泛化能力。

领域适应: 使用少量真实世界数据对仿真训练的模型进行微调。

元学习: 学习如何快速适应新环境的能力。

混合现实: 结合仿真和现实环境进行训练和测试。

## **具身智能的挑战与未来方向**

尽管具身智能研究取得了显著进展, 但仍面临诸多挑战, 同时也孕育着令人兴奋的未来发展方向:

**高质量机器人数据集的构建**  
获取足够的真实世界机器人数据仍然是一个重大挑战。单纯依赖模拟数据会加剧仿真到现实的差距问题。未来需要各研究机构之间紧密合作，创建多样化的真实世界机器人数据集。同时，开发更真实和高效的模拟器对于提高模拟数据的质量至关重要。

**人类示范数据的有效利用**

高效利用人类演示数据对于训练和改进机器人系统至关重要。这包括收集、处理和从大规模、高质量的数据集中学习，其中包含人类执行机器人需要学习的任务。未来的研究应关注如何有效利用大量非结构化、多标签和多模态的人类演示数据，结合动作标签数据来训练具身模型，使其能够在相对较短的时间内学习各种任务。

**复杂环境认知**  
具身智能体需要在物理或虚拟环境中感知、理解和导航复杂的现实世界环境。目前的工作通常依赖预训练的大语言模型进行简单任务规划，但缺乏对具体场景的深入理解。未来的研究应着重于增强知识转移和在复杂环境中的泛化能力，开发适应性强且可扩展的具身智能体架构。

**长程任务执行**  
执行复杂的长程任务，如 "打扫厨房", 需要机器人能够规划并执行一系列低级别动作，且持续较长时间。虽然当前的高级任务规划器已显示出初步的成功，但在多样化场景中仍显不足。未来需要开发具备强大感知能力和丰富常识知识的高效规划器。

**因果关系发现**  
现有的数据驱动的具身智能体主要基于数据内部的相关性做出决策，这种方法难以使模型真正理解知识、行为和环境之间的因果关系。未来的研究应关注如何使具身智能体以世界知识为驱动，具备自主的因果推理能力。

**持续学习**  
在机器人应用中，持续学习对于在多样化环境中部署机器人学习策略至关重要，但这一领域仍未被充分探索。未来的研究方向包括:

在新数据上进行微调时混合不同比例的先前数据分布，以缓解灾难性遗忘。

从先前分布或课程中开发有效的原型，用于新任务的推理学习。

提高在线学习算法的训练稳定性和样本效率。

确定将大容量模型无缝集成到控制框架中的原则性方法。

**统一评估基准**  
现有的评估基准在评估技能方面常常存在显著差异，且受到模拟器限制。未来需要使用逼真的模拟器开发涵盖多种技能的综合评估基准。特别是在评估长时间任务执行和成功率方面，需要综合评估高级任务规划器和低级控制策略的执行能力。

## **结论**

具身智能的发展使智能体能够更好地感知、认知并与数字空间和物理世界互动。这不仅将推动人工智能技术的进步，也将为解决现实世界中的各种挑战提供新的可能性。

**在应用方面，**具身智能有望在医疗康复、灾难救援、空间探索、精密制造等领域发挥重要作用。例如，在医疗领域, 具有高度灵活性和精确操作能力的具身智能机器人可能会协助进行复杂的手术；在灾难救援中，能够在危险环境中自主导航和决策的机器人可以大大提高救援效率和安全性。

然而，随着具身智能技术的发展，我们也需要关注**相关的伦理和安全问题**。如何确保具身智能系统的行为符合人类价值观，如何防止这些系统被滥用，如何在人机协作中保护人类的利益和隐私，都是需要深入探讨的问题。

总的来说，具身智能作为通向通用人工智能的关键路径，其研究不仅具有重要的科学意义，也蕴含着巨大的应用潜力。通过持续的创新和跨领域合作，**我们有望在不久的将来看到更加智能、灵活和可靠的具身智能系统，为人类社会带来深远的影响。**

----------------END----------------

**工业机器人企业**

[埃斯顿自动化](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3257349072756359172&scene=21#wechat_redirect) | [埃夫特机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3257353338380304393&scene=21#wechat_redirect) | [节卡机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3254648088418533381&scene=21#wechat_redirect) | [珞石机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3254663109932433416&scene=21#wechat_redirect) | [法奥机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286449098241556485&scene=21#wechat_redirect) | [非夕科技](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286451235054895108&scene=21#wechat_redirect) | [CGXi 长广溪智造](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293687153054662659&scene=21#wechat_redirect) | [大族机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286446214791774214&scene=21#wechat_redirect) |  [越疆机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286454601252290560&scene=21#wechat_redirect) | [睿尔曼智能](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286456343213850632&scene=21#wechat_redirect) | [优艾智合机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286455478348365826&scene=21#wechat_redirect) | [阿童木机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288958340173348870&scene=21#wechat_redirect) | [盈连科技](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293693334754115584&scene=21#wechat_redirect)

**服务与特种机器人企业**

[亿嘉和](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288954695272841217&scene=21#wechat_redirect) | [晶品特装](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288964066522382339&scene=21#wechat_redirect) | [九号机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3296726438896943115&scene=21#wechat_redirect) | [普渡机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288953102410399750&scene=21#wechat_redirect) | [机器姬](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288959037166010374&scene=21#wechat_redirect) | [猎户星空](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3403025009986240513#wechat_redirect) [|  七腾机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3403025009986240513#wechat_redirect)

**医疗机器人企业**

[元化智能](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293696134166822923&scene=21#wechat_redirect) | [天智航](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293721766665863172&scene=21#wechat_redirect) | [思哲睿智能医疗](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293724274507333641&scene=21#wechat_redirect) | [精锋医疗](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293725067264344065&scene=21#wechat_redirect) | [佗道医疗](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293726173956620290&scene=21#wechat_redirect) | [真易达](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293690023988641800&scene=21#wechat_redirect) | [术锐 ® 机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293727229444833285&scene=21#wechat_redirect) | [罗森博特](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293728506727841795&scene=21#wechat_redirect) | [磅客策](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293729257676029957&scene=21#wechat_redirect) | [柏惠维康](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293730015049891840&scene=21#wechat_redirect) [|](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293730015049891840&scene=21#wechat_redirect) [迪视医疗](https://mp.weixin.qq.com/s?__biz=MzI5MzE0NDUzNQ==&mid=2650358812&idx=2&sn=cad3275ca22a589fe96e3c8b1e531269&scene=21#wechat_redirect)

**人形机器人企业**

[优必选科技](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288979195142029317&scene=21#wechat_redirect) | [宇树](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288981594753679361&scene=21#wechat_redirect) | [达闼机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288950823108165633&scene=21#wechat_redirect) | [云深处](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288967267548086273&scene=21#wechat_redirect) | [理工华汇](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293731065135841287&scene=21#wechat_redirect) | [傅利叶智能](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288983966297047042&scene=21#wechat_redirect) | [逐际动力](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288985434051788809&scene=21#wechat_redirect) | [乐聚机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293731727953313793&scene=21#wechat_redirect) | [星动纪元](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293732259774283776&scene=21#wechat_redirect) | [天链机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3467475229234692100#wechat_redirect) | [中科深谷](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288997360286777350&scene=21#wechat_redirect)  | [大象机器人 |](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286447187786416133&scene=21#wechat_redirect) [伟景机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288992104941305856#wechat_redirect) | [众擎机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3568736079773564935#wechat_redirect) |  开普勒人形机器人

**具身智能企业**

[跨维智能](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3506492927482265606#wechat_redirect) | [银河通用](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3560375973176541192#wechat_redirect) | 千寻智能 | [方舟无限](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3541439704800280581#wechat_redirect) |  微亿智造

**核心零部件企业**

[绿的谐波](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288991540572536835&scene=21#wechat_redirect) | [因时机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288990101775269890&scene=21#wechat_redirect) | [脉塔智能](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293732796057993221&scene=21#wechat_redirect) | [锐驰智光](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288993384908668938&scene=21#wechat_redirect) | [地平线](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288995011610755083&scene=21#wechat_redirect) | [跨维智能](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3506492927482265606#wechat_redirect) | [本末科技](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3286444169649143812&scene=21#wechat_redirect) | [NOKOV 度量科技](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288996373115387911&scene=21#wechat_redirect) | [青瞳视觉](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288995537375150084&scene=21#wechat_redirect) | [因克斯](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293734699584143361&scene=21#wechat_redirect) | [蓝点触控](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293735422497603591&scene=21#wechat_redirect) | [福德机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3467267189910798341#wechat_redirect) | [巨蟹智能驱动](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3467268504405671937#wechat_redirect) |  鑫精诚传感器  | 思岚科技

**教育机器人企业**

[硅步机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3288998941606494211&scene=21#wechat_redirect) | [史河科教机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3293738917174919171&scene=21#wechat_redirect) | [大然机器人](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzI5MzE0NDUzNQ==&action=getalbum&album_id=3364759550264033287&scene=21#wechat_redirect)
