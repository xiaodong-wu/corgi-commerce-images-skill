# 可替换提示词

先将花括号变量替换为用户已确认内容。变量为空时删除对应段落，不让生成工具猜价格或数量。只生成用户要的图片，批量时每张图独立构造提示词。

## 共用风格段

```text
Use case: ads-marketing.
Create one square Chinese ecommerce service illustration.
Input images are STYLE REFERENCES ONLY: reference-cover controls the main-cover
visual identity; reference-scope controls information-card hierarchy.
Keep the same friendly tan-white corgi with blue neckerchief, cream and pale
sky-blue cloud background, navy outlines, glossy rounded oversized Chinese
headline, white sticker edges, and pastel pink/yellow/mint accent cards.
Use a polished cute 2D illustration, generous spacing, and crisp readable text.
Adapt the scene to {product_scene}. Do not copy reference product words or prices.
No watermark, account name, external contact, QR code, platform logo, fake
statistics, or promised outcomes. Add no promotional words beyond the exact text.
Use abstract lines instead of tiny invented words inside illustrative screens.
```

## 主图段

```text
Create the MAIN COVER.
Large headline in the upper half, exactly: "{headline}".
Price badge exactly: "{confirmed_price}".
Three short rounded chips exactly: "{tag_1}" / "{tag_2}" / "{tag_3}".
Bottom ribbon exactly: "{call_to_action}".
Lower-half scene: {product_scene}.
Keep the headline dominant, price secondary, corgi and product scene supporting.
```

没有价格时用 `Do not draw any price, currency symbol, or price badge.` 替换价格段。少于3个标签时按实际数量修改标签段。用户要其他比例时同步替换共用段的 `square`。

## 服务范围段

```text
Create a SERVICE SCOPE card.
Top product title exactly: "{headline}".
Large secondary heading exactly: "服务范围".
Three pastel cards with simple relevant icons and these exact texts:
"{object_and_quantity}" / "{required_materials}" / "{deliverables}".
Prominent bottom note exactly: "{scope_limit}".
Small footer exactly: "{confirmed_footer}".
No price on this image. No extra services, features, promises, or invented words.
```

`confirmed_footer` 可以是“具体交付与修改次数见商品说明”，但只在确有对应商品说明时使用。没有限制信息时删除底部限制段，不临时编造。

## 咨询交付段

```text
Create a PROCESS card using the same illustration style.
Headline exactly: "咨询与交付".
Four numbered steps exactly:
"发需求与资料" / "确认范围和时间" / "制作并检查" / "交付后核对".
Bottom ribbon exactly: "{channel_or_neutral_message}".
Small footer exactly: "{confirmed_footer}".
Keep the same corgi character, with clear readable numbered pastel cards.
Do not add delivery-time guarantees, refund promises, contact details, or logos.
```

普通渠道可用“确认需求后开始制作”；闲鱼任务且符合用户要求时可用“沟通交易都在闲鱼内”。步骤与文案都可按真实服务调整。

## 定点修图

```text
Edit the supplied image. Change ONLY {specific_problem} to {correct_text_or_fix}.
Preserve layout, colors, character, composition, and every other text element.
Do not add replacement slogans, decorations, or new claims.
```

## 完整小例子

- 产品：商品详情设计；价格：49元。
- 标签：3屏排版／卖点参数／图片交付。
- 场景：柯基在电脑前整理3张产品详情面板，产品为无品牌瓶子示意。
- 范围：1个商品·3屏详情图／使用你的产品图与文案／分屏PNG+拼接长图。
- 限制：不含拍摄精修与代发布。
- 行动提示：先发需求·确认范围后下单。

这是示例套餐，不是其他商品的默认服务范围或默认价格。
