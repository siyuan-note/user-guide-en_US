## Motivation
{: id="20201231085905-7m5lila"}

After choosing a note-taking app for a long time, I found that there is no note-taking app on the market that can meet these two requirements at the same time:
{: id="20201231085905-7nbq96v"}

* {: id="20201231085905-5vm3wnh"}Support standard Markdown and instant rendering. The sense of fragmentation brought about by the split-screen preview makes it difficult for me to fully focus on content creation
* {: id="20201231085905-zieszit"}Support block-level quoting and bidirectional linking. Through the block chain, I can find and organize existing content more efficiently, form a knowledge system and facilitate typesetting output
{: id="20201231085905-2l5np10"}

These two requirements are separated and there are ready-made products that can be realized, but once they are combined, there is no useful product. Since there is none, create one.
{: id="20201231085905-qge2vp2"}

## Storage format
{: id="20200924095851-u5jmzr3"}

In addition to the succinct syntax of Markdown's success, a big factor is that it is an open plain text format that can be opened for viewing and editing with a normal text editor. But with the increase of Markdown users, more "high-level" requirements gradually emerged. In order to meet these requirements, many projects have designed extended syntax based on the basic Markdown syntax.
{: id="20201231085905-morncyo"}

After a period of research and experimentation, we confirmed that using standard Markdown syntax (CommonMark/GFM) cannot achieve block-level reference, and an extended syntax must be introduced. Among the many Markdown extension syntaxes, we chose the [Inline Attribute Lists](https://kramdown.gettalong.org/syntax.html#inline-attribute-lists) provided by [kramdown](https://kramdown.gettalong.org) to identify block-level elements so that each block-level element has a unique ID. In this way, the block can be accurately obtained when referencing. Maximize versatility and interoperability while keeping Markdown text easy for humans to read and write.
{: id="20201231085905-4xwhtnk"}

Currently, there are not many platforms that support the kramdown extended syntax. If you need to publish the content of your notes to other platforms, you can use the export function to export standard Markdown files.
{: id="20201231085905-0ljc41w"}

## Local offline
{: id="20201231085905-mb8i60k"}

Note-taking applications should fully support offline use, only in this way can they be used to the greatest extent possible. For data synchronization needs, there are already many excellent solutions, such as various cloud disk services.
{: id="20201231085905-p4aszrg"}

Notes can be said to be the accumulation of knowledge in our life. From the perspective of usability and security, in the span of decades, no cloud notes can guarantee continuous availability, and the availability of local files is far greater than that of online applications. As long as local files are backed up (which can be regularly copied to other offline storage devices, or via cloud disks), they will basically not be lost or leaked. Cloud notes are different. There are many possibilities to cause data loss or leakage. It is basically unrealistic to use other mechanisms to back up. It can be said that the data in the cloud note is not under the control of the user.
{: id="20201231085905-oon4cys"}

The only advantage of using cloud notes is that it is convenient to share, but as a personal knowledge management tool, sharing is not just needed, or it is not a high-frequency demand. In summary, our conclusion is: **No offline, no notes**.
{: id="20201231085905-jculioi"}

## Embrace open source
{: id="20201231085905-sfk2wr3"}

After the data can be completely offline, there is one last problem left: the software life cycle.
{: id="20201231085905-7rya899"}

No software development team can guarantee the continuous availability of software. From the perspective of the development team, there are too many possibilities for software termination of maintenance, such as insufficient funds, transfer of R&D goals, or force majeure (such as the sudden death of the developer).
{: id="20201231085905-8bv2zqn"}

There is an effective way to solve the non-migration caused by software stoppage to the maximum extent, and that is **open source**. If the software has enough value and is completely open source, even if the main creative team can no longer maintain it, other developers can take over the important tasks. Starting from the actual situation of the development team, completely open source is relatively difficult to achieve. Although the open source commercialization model has been successful in many projects, not every project is suitable for this or needs to wait for the right time.
{: id="20201231085905-gz6g55t"}


{: id="20200924095830-rdxxx8n" type="doc"}
