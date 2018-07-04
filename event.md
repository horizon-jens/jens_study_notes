### Event 对象
Event 对象的属性提供了有关事件的细节（例如，事件在其上发生的元素）。Event 对象的方法可以控制事件的传播。

### 标准 Event 属性
| 属性 | 描述 |
|-|-|
| bubbles |	返回布尔值，指示事件是否是起泡事件类型。|
| cancelable |	返回布尔值，指示事件是否可拥可取消的默认动作。|
| currentTarget |	返回其事件监听器触发该事件的元素。|
| eventPhase |	返回事件传播的当前阶段。|
| target |	返回触发此事件的元素（事件的目标节点）。|
| timeStamp |	返回事件生成的日期和时间。|
| type |	返回当前 Event 对象表示的事件的名称。|

例子：
```javascript
//chrome点击事件对象
MouseEvent {
	altKey: false
	bubbles: true
	button: 0
	buttons: 0
	cancelBubble: false
	cancelable: true
	clientX: 237
	clientY: 558
	composed: true
	ctrlKey: false
	currentTarget: null
	defaultPrevented: false
	detail: 1
	eventPhase: 0
	fromElement: null
	isTrusted: true
	layerX: 237
	layerY: 32
	metaKey: false
	movementX: 0
	movementY: 0
	offsetX: 77
	offsetY: 33
	pageX: 237
	pageY: 558
	path:
		(9)[div.contact - btn, div.btm - box, div.page, body, shadow, document - fragment, html, document, Window]
	relatedTarget: null
	returnValue: true
	screenX: 454
	screenY: 746
	shiftKey: false
	sourceCapabilities: InputDeviceCapabilities {
		firesTouchEvents: true
	}
	srcElement: div.contact - btn
	target: div.contact - btn
	timeStamp: 196913.30000001471
	toElement: div.contact - btn
	type: "click"
	view: Window {
		postMessage: ƒ,
		blur: ƒ,
		focus: ƒ,
		close: ƒ,
		frames: Window,
		…
	}
	which: 1
	x: 237
	y: 558
}
```