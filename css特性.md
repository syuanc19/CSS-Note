# css特性

1.層疊性

- 概念: 如果樣式發生衝突，就會根據一定的規則(選擇器優先級)，進行樣式的層疊(覆蓋)

> 樣式衝突: 元素的`同一個樣式名`，被設置了`不同的值`，這就是衝突

2.繼承性

- 概念: 元素會自動擁有`其父元素`、或`其祖先元素`上所設置的`某些樣式`

- 規則: 優先繼承`離的近`的

  - 範例:

    ```css
    div {
        color:red;
    }
    p {
        color:purple;
    }
    ```

    ```html
    <div>
        div1
        <span>span1</span>
        <span>span2</span>
        <span>span3</span>
        <p>
            <span>span4</span>
        </p>
    <!-- 根據就近原則，span4離p較近，因此span4會繼承父親p的紫色，而其他span元素則是紅色 -->
    </div>
    ```

    

- 常見的可繼承屬性

> `text-??`, `font-??`, `line-??`, `color` ...

- 可以參照`MDN`網站查詢屬性是否可被繼承，在`VSC`裡，當鼠標懸停在元素時，可以點擊`MDN Reference`直連到`MDN`網站

<img src="https://github.com/syuanc19/picbed/blob/main/for%20css/image-20230828042927462.png?raw=true">

3.優先級

- 簡單說: !important > 行內樣式 > ID選擇器 > 類選擇器 > 元素選擇器 > 通配選擇器 > 繼承的樣式
> 計算權重時需要注意，`並級選擇器的每一個部分都是分開算的`
