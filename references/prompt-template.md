# 提示词模板

先确定保留区与处理区，再填入模板。只保留适用模式；花括号不是工具参数。

```text
Edit the supplied travel photograph into a vintage mixed-media torn-paper photo collage.
Output one standalone artwork at the source scene's {width:height} aspect ratio, not a before/after comparison.

INPUT ROLES
{Identify the actual editing target and style-only references.}
{Bundled references are TOP = finished collage, BOTTOM = original photograph. Learn visual treatment only from the top. Do not import their subjects, captions, watermark or split layout.}

MEMORY AND PRESERVATION
{Describe the meaningful moment and actual important people, poses, clothing, objects and spatial relationships.}
Preserve photographic recognizability in {specific regions}. Do not turn these people into illustrations or change their identity, age, attire or gestures.

REGION PLAN
Photographic regions to retain: {regions and why they matter}.
Environment that may be simplified: {specific regions}.
Warm aged-paper negative space: {specific regions}.
Primary technique: {select local single-color print treatment, simplified paper-shape background, or torn photographic window}.
{Optional supporting technique only if it materially helps.}

COLLAGE DESIGN
{Describe actual boundary paths, silhouettes and spatial connections.}
Natural uneven torn fibers and occasional narrow pale paper-core edges at selected photo/paper junctions. Avoid uniform zigzags or a white sticker outline around every object. Keep tears away from faces, hands, joints and important objects.
Predominantly flat printed collage, not thick layered relief or a shadow box.

COLOR AND MATERIAL
Warm beige aged paper with subtle fibers, restrained grain and gentle patina. Selective subdued or monochrome printed treatment in {regions}; retain useful photographic light and surface detail in {regions}.
One principal accent color, {color taken from the scene}, applied to {appropriate region}. Do not tint the whole photograph or obscure faces with dirt or grain.

TEXT
Exact small caption: "{place name + attraction, in pinyin or English, e.g. Longji Rice Terraces}"
Understated typewriter-style lettering in {natural paper negative space}, readable and slightly imperfect. No other text.
{Replace with no text if requested.}

AVOID
Full-image sepia filter, fully illustrated people, identity changes, thick paper sculpture, heavy drop shadows, plastic 3D, arbitrary decorations, tape, stamps, stickers, extra landmarks, copied reference objects, large title, UI, watermark and split panels.
```

## 用例判断

- 海边人物照：人物、坐姿与海面可保持摄影；复杂岸线纸片化，不能直接换成参考港口建筑。
- 手持纸币的山水照片：保留手势、纸币与山水关系，不因“简化”删除纪念物；可将部分山体和天空转换为纸面及印刷区域。
- 建筑风景无人物：建筑轮廓和地点是主体，选择保留局部摄影细节，不凭空添加人物；文案写「地名+景点名」（拼音或英文），如 Longji Rice Terraces，不写情绪化短句。
- 用户要求无字：完全取消默认短句，不保留模板文案。
- 用户要求脸部像素不变：按实际工具判断是否支持区域保护或合成，不能仅在提示词中写保持不变就报告完全达标。
- 无人物山水照片：大面积水面/反光默认转哑光单色印刷层（细密半调网点、纸底色调、无镜面高光）；山林转撕边纸片色块与树冠剪影；建筑轻度纸面化保留可辨识度；文案写「地名+景点名」（拼音或英文），如 Longji Rice Terraces。
