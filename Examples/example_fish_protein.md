# 🐟 案例展示：鱼蛋白抗冻 (深海坚盾降临)

本案例展示了如何通过农资宇宙的流水线，将“鱼蛋白肥料具有抗冻功效”这一农资卖点，转化为 15 秒的视觉大片脚本和 AI 提示词。

---

## 步骤一：选角 (从 01_Characters 中提取)
- **大地子民**：苹果树 (处于花期，极其脆弱)
- **破坏者**：倒春寒 (化身为冰霜巨魔)
- **守护者**：深海坚盾·鱼蛋白

## 步骤二：编剧大师出片 (`step1_script_writer.md`)

**【农资宇宙·微电影脚本：凛冬之战】**
**预计时长**：15秒

---
**🎬 第一幕：危机降临 (0-5秒)**
- **视觉画面**：阴云密布，狂风呼啸。一个由冰雪和寒气组成的巨大“冰霜巨魔”（倒春寒）在果园中肆虐。一棵盛开着粉色花朵的“苹果树”在寒风中瑟瑟发抖，娇嫩的花瓣边缘开始结出冰晶，生命光环逐渐暗淡。
- **镜头语言**：低角度仰视冰霜巨魔，压迫感极强；随后快速推镜头至苹果花结冰的微距特写。
- **音效/配音**：(音效) 刺骨寒风的呼啸声，冰块冻结的咔嚓声；(配音) 警报：遭遇极寒侵袭，生命体征下降！

**🎬 第二幕：英雄登场 (5-10秒)**
- **视觉画面**：天空突然破开一道深蓝色的光柱。身披流线型蓝色生物铠甲的“深海坚盾·鱼蛋白”从天而降，重重砸在苹果树前。他猛击地面，一道耀眼的蓝色能量波向四周扩散，瞬间在苹果树外围形成一个巨大的半透明抗冻能量罩，将冰雪彻底隔绝。
- **镜头语言**：跟随光柱的快速降落镜头，落地时带有轻微的屏幕震动（Screen Shake）；随后慢动作环绕拍摄能量护盾升起的瞬间。
- **音效/配音**：(音效) 巨大的重物落地轰鸣，能量护盾展开的高频声；(配音) 旁白：深海坚盾，全面激活！

**🎬 第三幕：逆转制胜 (10-15秒)**
- **视觉画面**：冰霜巨魔的攻击打在能量罩上纷纷碎裂，不甘地消散。护盾内的苹果花在蓝色光芒的滋养下，冰晶融化，花瓣变得更加鲜艳欲滴，散发出勃勃生机。画面最后定格在包装科技感十足的鱼蛋白产品上。
- **镜头语言**：由特写逐渐拉远为大远景，展现整个果园都在蓝色光盾的保护下安然无恙。
- **音效/配音**：(音效) 清脆的破冰声，温暖和煦的背景音；(配音) 旁白：XX鱼蛋白，锁定细胞温度，硬核抗冻！

---

## 步骤三：路径B - ComfyUI 专业工作流提示词 (`step2b_comfyui_prompt.md`)

## 工作流概览
- **大模型推荐**：SDXL 1.0
- **角色 LoRA**：（待建设，暂无）
- **采样器**：DPM++ 2M Karras
- **迭代步数**：28
- **CFG Scale**：7.5
- **生成尺寸**：1344x768（16:9）

---

### 幕次 1：危机降临

**正向提示词:**
`(giant frost troll made of ice and dark mist:1.5), (roaring in a dark orchard:1.3), macro shot of delicate pink apple blossoms freezing with detailed ice crystals on edges, dramatic stormy sky, cinematic lighting, dark and gloomy atmosphere, Unreal Engine 5 render style, hyper-detailed, masterpiece, best quality, 8k`

**反向提示词:**
`low quality, worst quality, blurry, deformed, mutated, extra limbs, bad anatomy, watermark, text, signature, jpeg artifacts, ugly, duplicate, morbid, mutilated, out of frame, error, warm lighting, cheerful atmosphere`

**参数建议:**
- 采样器：DPM++ 2M Karras
- 步数：28
- CFG：7.5
- 种子：-1（随机）
- Hires.fix：放大算法 R-ESRGAN 4x+，重绘幅度 0.35

**图生视频提示词 (AnimateDiff / SVD):**
`Macro camera slowly zooming in on pink apple blossom as frost and ice crystals form on its petals, dark background, wind blowing`

---
### 幕次 2：英雄降临

**正向提示词:**
`(futuristic superhero wearing glowing deep blue and silver bio-armor:1.5), (landing dynamically in front of an apple tree:1.4), (slamming the ground:1.3), massive glowing transparent blue energy shield dome protecting the tree, dark stormy background outside the shield, cinematic action shot, glowing rim light, high contrast, cyberpunk vibe, masterpiece, best quality, ultra-detailed, 8k`

**反向提示词:**
`low quality, worst quality, blurry, deformed, mutated, extra limbs, bad anatomy, watermark, text, signature, jpeg artifacts, ugly, duplicate, morbid, mutilated, out of frame, error, static pose, dull colors, low contrast, no shield`

**参数建议:**
- 采样器：DPM++ 2M Karras
- 步数：30
- CFG：8
- 种子：-1（随机）
- Hires.fix：放大算法 R-ESRGAN 4x+，重绘幅度 0.4

**图生视频提示词 (AnimateDiff / SVD):**
`Slow motion, superhero hits the ground and a glowing blue energy shield rapidly expands outwards, camera circling, screen shake effect`

---
### 幕次 3：逆转生机

**正向提示词:**
`(vibrant pink apple blossoms glowing with soft blue magical aura:1.5), (inside a protective transparent shield:1.3), frost melting away, warm cinematic lighting contrasting with dark cold outside, extreme macro, hyper-realistic, vivid colors, depth of field, masterpiece, best quality, 8k`

**反向提示词:**
`low quality, worst quality, blurry, deformed, mutated, extra limbs, bad anatomy, watermark, text, signature, jpeg artifacts, ugly, duplicate, morbid, mutilated, out of frame, error, dark gloomy lighting, frozen petals, cold colors`

**参数建议:**
- 采样器：DPM++ 2M Karras
- 步数：28
- CFG：7.5
- 种子：-1（随机）
- Hires.fix：放大算法 R-ESRGAN 4x+，重绘幅度 0.35

**图生视频提示词 (AnimateDiff / SVD):**
`Ice crystals melting quickly off the vibrant pink flower petals, soft glowing blue light pulsing, camera slowly pulling back to wide shot`
