#dynamic props

이전 영상은 hard coding된 props의 전달 과정이었는데, 

framework video는 사용법을 배우는 영상이라서 솔직히 그렇게 막 흥미가 돋진 않는다. 

```javascript


_getComments(){
	const commentList = [
		{id: 1, author: 'Morgan McCircuit', body: 'Great picture!'},
		{id: 2, author: 'Bending Bender', body: 'Excellent stuff'}
	];

	return commentList.map((comment) => {
			return(
				<comment author={comment.author}
							body={comment.body}
							key={comment.id} />);
	});
}

render(){
	const comments = this._getComments();
	return(
		<div className="comment-box">
			<h3>Comments</h3>
			<h4 className="comment-count">{comments.length} comments</h4>
			<div className="comment-list">
				{comments}
			</div>
		</div>
	);
}
```

how to pass dynamic props using variables

how to map object arrays to JSX arrays for display purposes

used javascript to handle plural case on the title