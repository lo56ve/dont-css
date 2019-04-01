<template>
    <dl class="div8">
		<dt class="dt">name:</dt>
		<dd class="dd">dont</dd>
		<dt class="dt">Email:</dt>
		<dd class="dd">dont@123.com</dd>
		<dt class="dt">Location:</dt>
		<dd class="dd">Shenzhen</dd>
	</dl>
</template>

<style scoped>
    .dd, .dt {
        display: inline;
    }
    /*在相邻第二个开始加*/
    .dd + .dt::before {
        /*0x000A相当于换行符，只写'\A'会和其他相邻空白换行符合并*/
        content: '\A';
        /*保留换行符*/
        white-space: pre;
    }
</style>
