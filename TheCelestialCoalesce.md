# The Celestial Coalesce

In a world where heaven and the earth dance in harmonious unity, there exists a celestial bond between Neel, the vast and majestic sky, and Rimjhim, the tender pattering rain. Their love story is one of enchantment, where every drop of rain carries the essence of Neel's affection.

![The Celestial Coalesce](https://github.com/sanam2405/sanam2405/blob/main/assets/images/design/design-4.png?raw=true)

Rimjhim, with her silver strands of raindrops, descends from the heaven above, drawn to the allure of Neel's vast expanse. With each tender touch, she caresses the earth, bestowing her blessings upon the world below.

Their romance is akin to a series of celestial events `E[N]` (0-indexed), where each event represents a precious moment they can share together. The events are marked by three elements as `E[i] = [start_day_i, end_day_i, affection_i]` where `i` is the `i-th` indexed event.

Here `start_day_i` represents the starting day of the `i-th` event, `end_day_i` represents the ending day of the `i-th` event, and `affection_i` represents the affection nourished due to the `i-th` event between Rimjhim and Neel.

When Rimjhim decides to attend an event (suppose the `i-th` indexed event), she is committed to it entirely, just as the rain embraces the earth without holding back. For each of the events attended by Rimjhim, the affection between Rimjhim and Neel increases by a value of `affection_i`.

Sadly, Rimjhim cannot attend multiple events with Neel simultaneously even if she wants to. She can only attend one event at a time. If she decides to attend an event, she has to attend the entire event. Note that the `end_day` is inclusive: that is, she cannot attend two events where one of them starts and the other ends on the same day.

Every event with Neel is a treasure, a testament to their love's depth and beauty. And yet, Rimjhim knows she can only attend a limited number of events. In this love tale, `K` represents the maximum number of events that Rimjhim can attend. Just as there are moments in life when we must choose between cherished experiences, Rimjhim too has to decide which events to grace with her presence and maximize the affection with Neel.

The total affection between Rimjhim and Neel is the summation of affection for all the events that Rimjhim decides to attend. So, Rimjhim wishes to choose `K` events at maximum so that the affection between the two gets maximized. Can you find the maximum affection Rimjhim and Neel can have if Rimjhim chooses at max `K` events optimally?

## Input

The first line consists of a positive integer `N` representing the total number of celestial events and `K` representing the maximum number of events that Rimjhim can attend.

- (1 <= K <= N, 1 <= K \* N <= 10^6)

The next `N` lines contain `N` events where each line contains an event in the form of three positive integers `start_day_i`, `end_day_i` and `affection_i`

- (1 <= start_day_i <= end_day_i <= 10^9, 1 <= affection_i <= 10^6)

## Output

Print the maximum affection that Rimjhim and Neel can have.

## Sample Test Case 1

**Input**

```shell
    4 3 1 1 1 2 2 2 3 3 3 4 4 4
```

**Output**

```shell
   9
```

**Explanation**: Although the events do not overlap, Rimjhim can only attend 3 events. Hence she attends the highest valued three events (4+3+2 = 9).

## Sample Test Case 2

**Input**

```shell
    3 2 1 2 4 3 4 3 2 3 10
```

**Output**

```shell
    10
```

**Explanation**: If Rimjhim attends the 0th and 1st indexed events, the affection they’ll have is (4+3 = 7). However, if she attends the 2nd indexed event only, they’ll have an affection of 10 which is the maximum affection they can have.

Note that Rimjhim cannot attend the 0th event and 2nd event simultaneously since for doing so, Rimjhim has to attend multiple events simultaneously on day 2, which is not allowed :(
