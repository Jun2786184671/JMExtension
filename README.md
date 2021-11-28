# JMExtension

**JMExtension is an Individually-developed Objectivec framework that is being refined.**

JMExtention is a light-weight ios framework that can improve productivity while keeping your code simple and clean, even without having to think about variable naming. JMExtension also absorbs the advantages of Masonry and Rac. It provides interfaces for reactive and functional programming, usesing blocks instead of delegates to decouple objects. You'll love it once you use it.

For examples take a look at the **JMExtension iOS Examples** project in the JMExtension workspace.

## What's the biggest headache for most developers?

I have to say that thinking about naming variables is a headache, and I'm guessing you spend a lot of time thinking about how to make your code look cleaner and more readable when programming. 
Imagine creating a cell with two image, one button, and four titles...
```obj-c
- (instancetype)initWithStyle:(UITableViewCellStyle)style reuseIdentifier:(NSString *)reuseIdentifier
{
    if (self = [super initWithStyle:style reuseIdentifier:reuseIdentifier]) {
        /** cell top container */
        UIView *topContainerView = [[UIView alloc] init];
        [self.contentView addSubview:topContainerView];
        self.topContainerView = topContainerView;
        /** image of head */
        UIImageView *headerImageView = [[UIImageView alloc] init];
        [self.topContainerView addSubview:headerImageView];
        self.headerImageView = headerImageView;
        /** image of photo */
        UIImageView *photoImageView = [[UIImageView alloc] init];
        [self.topContainerView addSubview:photoImageView];
        self.photoImageView = photoImageView;
        /** button of vip */
        UIButton *vipButton = [[UIButton alloc] init];
        [self.topContainerView addSubview:vipButton];
        self.vipButton = vipButton;
        /** label of name */
        UILabel *nameLabel = [[UILabel alloc] init];
        [self.topContainerView addSubview:nameLabel];
        self.nameLabel = nameLabel;
        /** label of time */
        UILabel *timeLabel = [[UILabel alloc] init];
        [self.topContainerView addSubview:timeLabel];
        self.timeLabel = timeLabel;
        /** label of source */
        UILabel *sourceLabel = [[UILabel alloc] init];
        [self.topContainerView addSubview:sourceLabel];
        self.sourceLabel = sourceLabel;
        /** label of content */
        UILabel *contentLabel = [[UILabel alloc] init];
        [self.topContainerView addSubview:contentLabel];
        self.contentLabel = contentLabel;
    }
    return self;
}
```
I have to say it's a bit annoying to look at code like this, but there's nothing wrong with it, and all ios developers write it like this. We spent a lot of time trying to figure out each variable, and even with detailed comments, the page was still confusing. And that's even when we don't have many views.

## Here comes JMExtension!

This is the code to create the same cell with JMExtension.
