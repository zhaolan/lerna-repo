<template>
 <badge :type="type" :inverted="inverted" :size="size" :text="text" />
</template>

<script>
import Badge from "@lanzhao-ui/badge"
/**
 * Badge 数字角标
 * @description 数字角标一般和其它控件（列表、9宫格等）配合使用，用于进行数量提示，默认为实心灰色背景
 * @tutorial https://ext.dcloud.net.cn/plugin?id=21
 * @property {String} text 角标内容
 * @property {String} type = [default|primary|success|warning|error] 颜色类型
 * 	@value default 灰色
 * 	@value primary 蓝色
 * 	@value success 绿色
 * 	@value warning 黄色
 * 	@value error 红色
 * @property {String} size = [normal|small] Badge 大小
 * 	@value normal 一般尺寸
 * 	@value small 小尺寸
 * @property {String} inverted = [true|false] 是否无需背景颜色
 * @event {Function} click 点击 Badge 触发事件
 * @example <uni-badge text="1"></uni-badge>
 */
export default {
  name: 'UniBadge',
  components: {Badge},
  props: {
    type: {
      type: String,
      default: 'default'
    },
    inverted: {
      type: Boolean,
      default: false
    },
    text: {
      type: [String, Number],
      default: ''
    },
    size: {
      type: String,
      default: 'normal'
    }
  },
  data() {
    return {
      badgeStyle: ''
    };
  },
};
</script>

<style lang="less" scoped>

</style>
