## Type field `type`
{: id="20210210104024-efd1ar6"}

The search condition supports expressions, you can use the `type:x` syntax to enable type filtering, where the value of `x` is as follows:
{: id="20201224120448-hggh9p6"}

* {: id="20201224120448-mpmfni9"}`d` Document block (Only search on the document name, will not search for the document containing content blocks)
  {: id="20210210104014-pbdtm4z"}
* {: id="20201224120448-x5dqp91"}`h` Heading block (Search only on the heading name, not the content blocks below the heading block)
  {: id="20210210104014-u6dnfps"}
* {: id="20201224120448-gl1j8m7"}`l` List block (including ordered list block, unordered list block and task list block)
  {: id="20210210104014-2iglz5u"}
* {: id="20201224120448-82e30qt"}`i` List item block
  {: id="20210210104014-kgaw1ni"}
* {: id="20201224120448-2eln6e1"}`c` Code block
  {: id="20210210104014-hp14o29"}
* {: id="20201224120448-n8mu5sk"}`m` Mathematical formula block
  {: id="20210210104014-zy55cgi"}
* {: id="20201224120448-1ijl3c0"}`t` Table block
  {: id="20210210104014-ptxclb2"}
* {: id="20201224120448-c7ah3jj"}`b` Blockquote block
  {: id="20210210104014-ibm76xn"}
* {: id="20201224120448-d1kiaru"}`s` Super block
  {: id="20210210104014-kod2ag3"}
* {: id="20201224120448-p3d5s2n"}`p` Paragraph block
  {: id="20210210104014-c3xubz3"}
{: id="20201224092621-haejkkh"}

For example, if you want to search all title blocks that contain `Markdown`, you can use `Markdown type:h`, abbreviated as `h:Markdown`.
{: id="20201224120448-iaarh39"}

## Subtype field `subtype`
{: id="20210210104037-xex9wds"}

List block / List item block subtypes:
{: id="20210210104044-84398d1"}

* {: id="20210210104131-x6ccpvv"}`o`：Ordered
  {: id="20210210104131-y14edfl"}
* {: id="20210210104131-12dy0vx"}`u`：Unordered
  {: id="20210210104131-90lbr4w"}
* {: id="20210210104131-kegiok1"}`t`：Task
  {: id="20210210104131-nexfzd6"}
{: id="20210210104132-vh0vm5r"}

Heading subtypes:
{: id="20210210104145-8m1u1xh"}

* {: id="20210210104208-rxp06ei"}`h1`: Level 1
  {: id="20210210104208-uv7t9t9"}
* {: id="20210210104208-dllfrj1"}`h2`: Level 2
  {: id="20210210104208-2o8p40d"}
* {: id="20210210104208-qamuu48"}`h3`: Level 3
  {: id="20210210104208-8ug6ogo"}
* {: id="20210210104208-fp538km"}`h4`: Level 4
  {: id="20210210104208-01bwpvx"}
* {: id="20210210104208-8e3c07q"}`h5`: Level 5
  {: id="20210210104208-hl0xh7i"}
* {: id="20210210104208-ev1v2rt"}`h6`: Level 6
  {: id="20210210104208-eilwj50"}
{: id="20210210104208-7j0si3s"}

Other types of content blocks have no subtypes.
{: id="20210210104208-cqh7hul"}


{: id="20201222100222-q47d64s" type="doc"}
