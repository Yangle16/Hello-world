# Hello-world
<?php
/**
 * 冒泡排序
 *
 * @param &$list array 待排序数组
 *
 */
function bubbleSort(&$list) {
	//控制轮数
	for($i=1,$list_len=count($list); $i<$list_len; ++$i) {
		//参与比较的元素下标
		for($k=0; $k<=$list_len-1-$i; ++$k) {
			//比较，$k 与 $k+1元素做比较
			if($list[$k] > $list[$k+1]) {
				//交换
				$tmp = $list[$k];
				$list[$k] = $list[$k+1];
				$list[$k+1] = $tmp;
			}
		}
	}
//	return true;
}
$list = array(24, 11, 67, 10, 9, 23, 45);
bubbleSort($list);

var_dump($list);

?>
