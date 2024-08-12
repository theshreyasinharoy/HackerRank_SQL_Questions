# Top Competitors

#### Julia just finished conducting a coding contest, and she needs your help assembling the leaderboard! Write a query to print the respective hacker_id and name of hackers who achieved full scores for more than one challenge. Order your output in descending order by the total number of challenges in which the hacker earned a full score. If more than one hacker received full scores in same number of challenges, then sort them by ascending hacker_id.

#### Input Format

#### The following tables contain contest data:
#### - Hackers: The hacker_id is the id of the hacker, and name is the name of the hacker.

![Hackers](https://github.com/user-attachments/assets/d1827e14-e0ff-433a-905e-26a23dc71174)

#### Solution:-
```
SELECT
          h.hacker_id, h.name
FROM
          Hackers h
          JOIN Submissions s ON h.hacker_id = s.hacker_id
          JOIN Challenges c ON s.challenge_id = c.challenge_id
          JOIN Difficulty  d ON c.difficulty_level = d.difficulty_level
WHERE
          s.score = d.score
GROUP BY
          h.hacker_id, h.name
HAVING
          COUNT(c.challenge_id) > 1
ORDER BY
          COUNT(c.challenge_id) DESC, h.hacker_id ASC; 
```
