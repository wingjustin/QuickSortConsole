# QuickSortConsole

<h3>快速排序</h3>

<p>
重複元素少用二路排序, 重複元素多用三路排序
<br><br>
  <div>pivot 選點策略為三數中值法 : 
    <br>每次選點前先把首個元素,最尾元素和中間元素 進行簡單排序, 排序後放回對應位置, 並取三個數的中位數為pivot</div>
  <br><br>
<div>二路排序</div>
<ul>
<li>設定 l 為左指針, r 為右指針, 完成一次遞迴操作時 l指針的左邊所有元素為小於pivot, r指針的右邊所有元素為大於pivot, 所以l指針和r指針交錯位置為pivot的正確位置</li>
<br>
<li>理想情況下第一層操作要掃描n個元素來處理一個pivot元素的移到正確位置
<br>, 到第二層處理一個pivot元素只需掃描n/2個元素, 所以第二層掃描n個元素後可以處理兩個元素, 一共處理了三個元素
<br>, 到第三層可以處理四個元素, 一共處理了七個元素
<br>, 到第k層可以處理2^(k-1)個元素, 一共處理了2^k - 1個元素</li>
<br>
<li>所以理想時間複雜度為O(nlogn)。</li>
</ul>

<div>三路排序</div>
<ul>
  <li>分三個區域,左邊為小於pivot, 中間為等於pivot, 右邊為大於pivot</li>
  <br>
<li>設定 lo 為左指針,分隔左區與中間, hi 為右指針,分隔中間與右區, i 為當前指針
  <br>, 移動i逐一掃描元素, 把小於pivot移去左區, 把大於pivot移去右區, </li>
<br>
  <li>完成一次遞迴操作時 lo指針的左邊所有元素為小於pivot, hi指針的右邊所有元素為大於pivot, lo指針和hi指針之間為pivot和所有等於pivot的元素的正確位置</li>
<br>
<li>進入下一層遞迴時可以忽略中間區域,加快速度</li>
</ul>

<div>reference :</div>
<ul>
  <li>https://blog.csdn.net/qq_29110265/article/details/83502450</li>
  <li>https://blog.csdn.net/Bob__yuan/article/details/98782859</li>
  </ul>
</p>
