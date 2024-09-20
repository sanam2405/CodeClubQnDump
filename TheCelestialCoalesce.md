# The Celestial Coalesce

In a world where heaven and the earth dance in harmonious unity, there exists a celestial bond between _Neel_, the vast and majestic sky, and _Rimjhim_, the tender pattering rain. Their love story is one of enchantment, where every drop of rain carries the essence of _Neel_'s affection.

![The Celestial Coalesce](https://github.com/sanam2405/sanam2405/blob/main/assets/images/design/design-4.png?raw=true)

_Rimjhim_, with her silver strands of raindrops, descends from the heaven above, drawn to the allure of _Neel_'s vast expanse. With each tender touch, she caresses the earth, bestowing her blessings upon the world below.

Their romance is akin to a series of celestial events $E[N]$ (0-indexed), where each event represents a precious moment they can share together. The events are marked by three elements as $E[i] = [\textit{startDay}_i, \textit{endDay}_i, \textit{affection}_i]$ where $i$ is the $i$-th indexed event.

Here $\textit{startDay}_i$ represents the starting day of the $i$-th event, $\textit{endDay}_i$ represents the ending day of the $i$-th event, and $\textit{affection}_i$ represents the affection nourished due to the $i$-th event between _Rimjhim_ and _Neel_.

When _Rimjhim_ decides to attend an event (suppose the $i$-th indexed event), she is committed to it entirely, just as the rain embraces the earth without holding back. For each of the events attended by _Rimjhim_, the affection between _Rimjhim_ and _Neel_ increases by a value of $\textit{affection}_i$.

Sadly, _Rimjhim_ cannot attend multiple events with _Neel_ simultaneously even if she wants to. She can only attend one event at a time. If she decides to attend an event, she has to attend the entire event. Note that the $\textit{endDay}$ is inclusive: that is, she cannot attend two events where one of them starts and the other ends on the same day.

Every event with _Neel_ is a treasure, a testament to their love's depth and beauty. And yet, _Rimjhim_ knows she can only attend a limited number of events. In this love tale, $K$ represents the maximum number of events that _Rimjhim_ can attend. Just as there are moments in life when we must choose between cherished experiences, _Rimjhim_ too has to decide which events to grace with her presence and maximize the affection with _Neel_.

The total affection between _Rimjhim_ and _Neel_ is the summation of affection for all the events that _Rimjhim_ decides to attend. So, _Rimjhim_ wishes to choose $K$ events at maximum so that the affection between the two gets maximized. Can you find the maximum affection _Rimjhim_ and _Neel_ can have if _Rimjhim_ chooses at most $K$ events optimally?

## Input

The first line consists of a positive integer $N$ representing the total number of celestial events and $K$ representing the maximum number of events that _Rimjhim_ can attend.

- $(1 \leq K \leq N, 1 \leq K \times N \leq 10^6)$

The next $N$ lines contain $N$ events where each line contains an event in the form of three positive integers $\textit{startDay}_i$, $\textit{endDay}_i$ and $\textit{affection}_i$

- $(1 \leq \textit{startDay}_i \leq \textit{endDay}_i \leq 10^9, 1 \leq \textit{affection}_i \leq 10^6)$

## Output

Print the maximum affection that _Rimjhim_ and _Neel_ can have.

## Sample Test Case 1

**Input**

```shell
    4 3
    1 1 1
    2 2 2
    3 3 3
    4 4 4
```

**Output**

```shell
   9
```

**Explanation**: Although the events do not overlap, _Rimjhim_ can only attend 3 events. Hence she attends the highest valued three events $(4+3+2 = 9)$.

## Sample Test Case 2

**Input**

```shell
    3 2
    1 2 4
    3 4 3
    2 3 10
```

**Output**

```shell
    10
```

**Explanation**: If _Rimjhim_ attends the 0th and 1st-indexed events, the affection they’ll have is $(4+3 = 7)$. However, if she attends the 2nd-indexed event only, they’ll have an affection of 10 which is the maximum affection they can have.

Note that _Rimjhim_ cannot attend the 0th event and 2nd event simultaneously since for doing so, _Rimjhim_ has to attend multiple events simultaneously on day 2, which is not allowed :(
