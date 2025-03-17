<%*
const moment = window.moment; // 使用 Templater 内置的 moment.js
let month = tp.date.now("M") - 1; // 当前月份（0-11）
let year = tp.date.now("YYYY"); // 当前年份
let daysInMonth = moment({ year: year, month: month }).daysInMonth(); // 当月天数
let monthName = moment({ year: year, month: month }).format("MMMM"); // 月份名称
-%>

以上标粗体的部分是我不认识的单词，请帮我给出每个单词的释义，包括词性，释义，发音，并给我一个区别于上文的例句，例句尽可能剪短一些
# English Learning - {{monthName}} {{year}}

## Instructions
To use this template:
1. This file tracks daily English learning for {{monthName}} {{year}}.
2. Fill in the learning content for each day below.
3. Complete the "Monthly Reflection" at the end of the month.

<%*
for (let day = 1; day <= daysInMonth; day++) {
  let dayDate = moment({ year: year, month: month, day: day }).format("MMMM D, YYYY");
  tR += `## ${dayDate}\n- Source:\n- New Vocabulary:\n- Sentences:\n- Notes:\n\n`;
}
-%>

## Monthly Reflection
- What did I learn this month?
- What are my strengths and areas for improvement?
- Any goals for next month?